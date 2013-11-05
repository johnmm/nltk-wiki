Answers to Frequently Asked Questions about NLTK

<p><i>Do you have a question that is not answered here?  Please post it to the <a href="http://groups.google.com/group/nltk-users">nltk-users</a> mailing list.</i> </p><ol><li><b>What license does NLTK use?</b> </li><blockquote>NLTK is open source software.  The source code is distributed under the 
terms of the <a href="http://www.apache.org/licenses/LICENSE-2.0" rel="nofollow">Apache License Version 2.0</a>.  The documentation is distributed under the terms of the 
<a href="http://creativecommons.org/licenses/by-nc-nd/3.0/us/" rel="nofollow">Creative Commons Attribution-Noncommercial-No Derivative Works 3.0 United States license</a>. 
The corpora are distributed under various licenses, as documented in their respective README files. 
</blockquote><li><b>What are the plans for further development of NLTK?</b> </li><blockquote>NLTK is undergoing continual development as new modules are added and existing ones are improved.  Now that NLTK 2.0 (beta) has been released we will be following a conservative upgrade process, and ensure that all code examples published in the NLTK book continue to work as advertized.  We will follow the recommended migration path for Python 
3.0.<br /></blockquote><li><b>I think I found a bug; where do I report it?</b> </li><blockquote>Please check if an issue report has already been filed by searching the <a href="http://code.google.com/p/nltk/issues/list" rel="nofollow">Issue Tracker</a>.  If not, please report the problem, giving 
as much detail as possible.  Please include a code sample that 
permits us to replicate the problem. 
</blockquote><li><b>What data sources does NLTK use and how can more be added?<br /></b><div style="margin-left:40px"><br />Dozens of corpora are available for use with NLTK (see the list of <a href="https://sites.google.com/site/naturallanguagetoolkit/data.1383616540445">available datasets</a>, and the <a href="http://nltk.googlecode.com/svn/trunk/doc/howto/corpus.html">Corpus HOWTO</a>).  NLTK can be interfaced to other corpora; for instructions see section 2.1 of the <a href="https://sites.google.com/site/naturallanguagetoolkit/book.1383614193214">NLTK book</a>, and consult the code in the <a href="http://code.google.com/p/nltk/source/browse/trunk/nltk/nltk/corpus#corpus/reader">corpus module</a>.  Requests for advice in developing corpus readers for new formats should be posted to the <a href="http://groups.google.com/group/nltk-dev">nltk-dev mailing list</a>.  Completed corpus readers should be submitted via the <a href="http://code.google.com/p/nltk/issues/list" rel="nofollow">Issue Tracker</a>.  Please specify the location of the corpus and whether it can be redistributed with NLTK.<br /><br /></div></li><li><b>I'm planning some long-term research using NLTK; how long is the toolkit going to be supported?</b> </li><blockquote>We plan to continue supporting the toolkit for as long as 
possible.  We published the NLTK book in 2009 and plan to 
support the toolkit for several years while the book is in active 
use, and while the developers are employed to teach natural 
language processing.  Bug reports will be attended 
to as quickly as possible. 
</blockquote><li><b>Why is Python giving me a syntax error when I use NLTK?</b> </li><blockquote>NLTK requires Python version 2.5, 2.6, or 2.7.  If you use an earlier 
version of Python you will see many syntax errors.<br /></blockquote><li><b>What is the difference between NLTK and NLTK-Lite?</b> </li><blockquote>Since mid-2005, the NLTK developers have been creating a 
lightweight version of NLTK, called NLTK-Lite. NLTK-Lite is 
simpler and faster than NLTK. Once it is complete, NLTK-Lite will 
provide the same functionality as NLTK (in fact, all of NLTK 
functionality is now in NLTK-Lite 0.9, and the package is called 
nltk). Unlike the old NLTK, NLTK-Lite does not impose such a heavy 
burden on the programmer. Wherever possible, standard Python 
objects are used instead of custom NLP versions, so that students 
learning to program for the first time will be learning to program 
in Python with some useful libraries, rather than learning to 
program in NLTK.  Once it reached version 1.0 (in mid 2009), 
NLTK-Lite took over the original NLTK name, and became NLTK 
2.0. 
</blockquote><li><b>How can I install NLTK from the source code repository?</b> </li><blockquote>Most users should install NLTK from a distribution.  Please see 
the <a href="https://sites.google.com/site/naturallanguagetoolkit/download.1383615362424">installation instructions</a>.  However, if you need 
an up-to-the-minute version, then you will have to install NLTK 
from the <a href="http://code.google.com/p/nltk/source/checkout" rel="nofollow">source repository</a>. 
Once you've downloaded this, you'll need to run the 
top level setup.py program to install this version of NLTK on your 
machine. 
</blockquote><li><b>How can I find out where NLTK is installed on my system?</b> </li><blockquote>Do the following in a Python interpreter session.  In this case we 
see that NLTK is installed in <tt>/Library/Python/2.5/site-packages/nltk</tt>
<pre><span>&gt;&gt;&gt;</span><span> </span><span>import</span><span> nltk<br /></span><span>&gt;&gt;&gt;</span><span> nltk</span><span>.</span><span>__path__<br /></span><span>[</span><span>'/Library/Python/2.5/site-packages/nltk'</span><span>]</span></pre></blockquote><li><b>What papers have been published about NLTK?</b> </li><blockquote>NLTK has been presented at several academic conferences, and 
reviewed in online forums.  Please see the <a href="https://sites.google.com/site/naturallanguagetoolkit/documentation.1383616523265">Documentation</a> page 
for more information. 
</blockquote><li><b>How is NLTK development supported?</b> </li><blockquote>NLTK is an open source project that depends mainly on the efforts 
of volunteers.  Occasionally we have funds for a summer intern or 
TA to work on specified projects.  Students and teachers also 
donate code.  In 2008 , we received support from <i>Google 
Summer of Code</i>.  We strongly encourage volunteers to get 
involved: <a href="http://www.nltk.org/contribute" rel="nofollow">find out more about contributing to NLTK</a>. 
If you find the toolkit useful, please make a donation to 
support further development. 
</blockquote><li><b>How did NLTK start?</b> </li><blockquote>The NLTK project began when Steven Bird was teaching CIS-530 at 
the University of Pennsylvania in 2001, and hired his star 
student, Edward Loper, from the previous offering of the course to 
be the teaching assistant (TA).  They agreed a plan for developing 
software infrastructure for NLP teaching that could be easily 
maintained over time.  Edward wrote up 
<a href="http://code.google.com/p/nltk/source/browse/trunk/nltk-old/doc/technical/proposal/proposal.tex" rel="nofollow">the plan</a>, 
and both began work on it right away.  Here is the 
<a href="http://sourceforge.net/mailarchive/forum.php?thread_id=22772&amp;amp;forum_id=960" rel="nofollow">Version 0.2 release announcement</a> 
that appeared in September 2001. 
</blockquote><li><b>If I just "use" NLTK using import statements in Python, am I obliged to publish my source code as well?</b> </li><blockquote>No, there is no such obligation.  You can use and modify NLTK without making any code available (see question 1).</blockquote><li><b>What is Natural Language Processing?</b> </li><blockquote>Please see our <a href="https://sites.google.com/site/naturallanguagetoolkit/book.1383614193214">book</a>, or <a href="http://en.wikipedia.org/wiki/Natural_language_processing" rel="nofollow">http://en.wikipedia.org/wiki/Natural_language_processing</a>
</blockquote></ol></div></td></tr></tbody></table>
</div>