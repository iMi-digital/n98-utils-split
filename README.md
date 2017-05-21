N98-Utils-Split
===============

Split of N98/Utils from the Magerun1 repository

How It Is done
==============

	cd ../n98-magerun
	git subtree split -P src/N98/Util/ -b split-src-n98-util
	git subtree split -P tests/N98/Util -b split-tests-n98-util
	git subtree split -P shared/src/N98/Util -b split-shared-src-n98-util
	git subtree split -P shared/tests/N98/Util -b split-shared-tests-n98-util
	cd ../n98-utils-split

	# on the first run
	# git remote add magerun ../n98-magerun
	git fetch magerun

	# on the first run
	# git subtree add -P src/N98/Util/ magerun/split-src-n98-util
	# git subtree add -P tests/N98/Util/ magerun/split-tests-n98-util

	# git subtree add -P shared/src/N98/Util/ magerun/split-shared-src-n98-util
	# git subtree add -P shared/tests/N98/Util/ magerun/split-shared-tests-n98-util

	git subtree merge -P src/N98/Util/ magerun/split-src-n98-util
	git subtree merge -P tests/N98/Util/ magerun/split-tests-n98-util
	git subtree merge -P shared/src/N98/Util/ magerun/split-shared-src-n98-util
	git subtree merge -P shared/tests/N98/Util/ magerun/split-shared-tests-n98-util

