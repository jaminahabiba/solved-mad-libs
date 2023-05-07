Download Link: https://assignmentchef.com/product/solved-mad-libs
<br>
<a href="https://www.youtube.com/playlist?list=PLhOuww6rJJNPnNx_Emds00y2RX1Tbk59r" rel="nofollow">https://www.youtube.com/playlist?list=PLhOuww6rJJNPnNx_Emds00y2RX1Tbk59r</a>

Write a “Mad Libs” program that will read a given file and prompt the user for the parts of speech indicated in angle brackets, e.g., <code>&lt;verb&gt;</code>, replacing those values and printing the new text a la the beloved “Mad Libs” game. For example, the input file might look like this:

<pre><code>$ cat inputs/fox.txtThe quick &lt;adjective&gt; &lt;noun&gt; jumps &lt;preposition&gt; the lazy &lt;noun&gt;.</code></pre>

When run with this input, the program would prompt the user for “adjective,” “noun,” etc. When all the answers have been collected, the new text will be printed:

<pre><code>$ ./mad.py inputs/fox.txtGive me an adjective: scaryGive me a noun: chairGive me a preposition: behindGive me a noun: skyThe quick scary chair jumps behind the lazy sky.</code></pre>

In order to test, the program should also accept all the values as <code>-i</code> or <code>--inputs</code>:

<pre><code>$ ./mad.py inputs/fox.txt -i scary chair behind skyThe quick scary chair jumps behind the lazy sky.</code></pre>

If provided no arguments, the program should print a brief usage:

<pre><code>$ ./mad.pyusage: mad.py [-h] [-i [str [str ...]]] FILEmad.py: error: the following arguments are required: FILE</code></pre>

Or a longer usage for <code>-h</code> or <code>--help</code>:

<pre><code>$ ./mad.py -husage: mad.py [-h] [-i [str [str ...]]] FILEMad Libspositional arguments:  FILE                  Input fileoptional arguments:  -h, --help            show this help message and exit  -i [str [str ...]], --inputs [str [str ...]]                        Inputs (for testing) (default: None)</code></pre>

Run the test suite to ensure your program is working correctly:

<pre><code>$ make testpytest -xv test.py============================= test session starts ==============================...collected 7 itemstest.py::test_exists PASSED                                              [ 14%]test.py::test_usage PASSED                                               [ 28%]test.py::test_bad_file PASSED                                            [ 42%]test.py::test_no_blanks PASSED                                           [ 57%]test.py::test_fox PASSED                                                 [ 71%]test.py::test_help PASSED                                                [ 85%]test.py::test_verona PASSED                                              [100%]============================== 7 passed in 0.65s ===============================</code></pre>