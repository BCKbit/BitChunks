Compiling/running bitchunksd unit tests
------------------------------------

bitchunksd unit tests are in the `src/test/` directory; they
use the Boost::Test unit-testing framework.

To compile and run the tests:

	cd src
	make -f makefile.unix test_bitchunks  # Replace makefile.unix if you're not on unix
	./test_bitchunks   # Runs the unit tests

If all tests succeed the last line of output will be:
`*** No errors detected`

To add more tests, add `BOOST_AUTO_TEST_CASE` functions to the existing
.cpp files in the test/ directory or add new .cpp files that
implement new BOOST_AUTO_TEST_SUITE sections (the makefiles are
set up to add test/*.cpp to test_bitchunks automatically).


Compiling/running BitChunks-Qt unit tests
---------------------------------------

BitChunks-Qt unit tests are in the src/qt/test/ directory; they
use the Qt unit-testing framework.

To compile and run the tests:

	qmake bitchunks-qt.pro BITCOIN_QT_TEST=1
	make
	./bitchunks-qt_test

To add more tests, add them to the `src/qt/test/` directory,
the `src/qt/test/test_main.cpp` file, and bitchunks-qt.pro.
