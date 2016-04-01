Answers to Frequently Asked Questions about NLTK

<p><i>Do you have a question that is not answered here?  Please post it to the <a href="http://groups.google.com/group/nltk-users">nltk-users</a> mailing list.</i></p>

<ol><li><b>What license does NLTK use?</b> </li><blockquote>NLTK is open source software.  The source code is distributed under the 
terms of the <a href="http://www.apache.org/licenses/LICENSE-2.0" rel="nofollow">Apache License Version 2.0</a>.  The documentation is distributed under the terms of the 
<a href="http://creativecommons.org/licenses/by-nc-nd/3.0/us/" rel="nofollow">Creative Commons Attribution-Noncommercial-No Derivative Works 3.0 United States license</a>. 
The corpora are distributed under various licenses, as documented in their respective README files. 
</blockquote>
<li><b>What are the plans for further development of NLTK?</b> </li><blockquote>NLTK is undergoing continual development as new modules are added and existing ones are improved.  NLTK 3.0 has been finalized, and we have updated the code samples in the NLTK book.</blockquote>
<li><b>I think I found a bug; where do I report it?</b> </li><blockquote>Please check if an issue report has already been filed by searching the <a href="https://github.com/nltk/nltk/issues" rel="nofollow">Issue Tracker</a>.  If not, please report the problem, giving 
as much detail as possible.  Please include a code sample that 
permits us to replicate the problem. </blockquote>
<li><b>How can I contribute to NLTK development?</b></li><blockquote>New contributions are always welcome. Please consult the <a href="https://github.com/nltk/nltk/wiki#development">list of development priorities</a> and the <a href="https://github.com/nltk/nltk/issues">issue tracker</a> and submit a pull request. If you have particular expertise to offer, or new functionality to propose, please describe it on the <a href="https://groups.google.com/forum/#!forum/nltk-dev">nltk-dev mailing list</a>.</blockquote>
<li><b>What data sources does NLTK use and how can more be added?</b></li><blockquote>Dozens of corpora are available for use with NLTK (see the list of <a href="http://nltk.org/nltk_data/">available datasets</a>, and the <a href="http://nltk.org/howto/">Corpus HOWTO</a>).  NLTK can be interfaced to other corpora; for instructions see section 2.1 of the <a href="http://nltk.org/book/ch02.html">NLTK book</a>, and consult the code in the <a href="https://github.com/nltk/nltk/tree/master/nltk/corpus/reader">corpus module</a>.  Requests for advice in developing corpus readers for new formats should be posted to the <a href="http://groups.google.com/group/nltk-dev">nltk-dev mailing list</a>.  Completed corpus readers should be submitted via the <a href="http://code.google.com/p/nltk/issues/list" rel="nofollow">Issue Tracker</a>.  Please specify the location of the corpus and whether it can be redistributed with NLTK.</blockquote>
<li><b>I'm planning some long-term research using NLTK; how long is the toolkit going to be supported?</b> </li><blockquote>We plan to continue supporting the toolkit for as long as 
possible.  We published the NLTK book in 2009 and a second edition is due out in 2016.
We plan to support the toolkit while the book is in active 
use, and while the developers are employed in NLP research and teaching.
Bug reports will be dealt with as quickly as possible. 
</blockquote><li><b>Why is Python giving me a syntax error when I use NLTK?</b> </li><blockquote>NLTK requires Python version 2.7, or Python 3.2 onwards.  If you use an earlier 
version of Python you will see many syntax errors.<br /></blockquote>
<li><b>What is the difference between NLTK and NLTK-Lite?</b> </li><blockquote>In mid-2005, the NLTK developers created a 
lightweight version of NLTK called NLTK-Lite. NLTK-Lite was 
simpler and faster than NLTK at that time. As of version 0.9, NLTK-Lite 
provided the same functionality as NLTK. Unlike the old NLTK, NLTK-Lite did not impose such a heavy 
burden on the programmer. Wherever possible, standard Python 
objects were adopted instead of custom NLP versions, so that students 
learning to program for the first time would be learning to program 
in Python with some useful libraries, rather than learning to 
program in NLTK.  Once it reached version 1.0 (in mid 2009), 
NLTK-Lite took over the original NLTK name and became NLTK 
2.0. 
</blockquote><li><b>How can I install NLTK from the source code repository?</b> </li><blockquote>Most users should install NLTK from a distribution.  Please see 
the <a href="http://nltk.org/install.html">installation instructions</a>.  However, if you need 
an up-to-the-minute version, then you will have to install NLTK 
from the <a href="https://github.com/nltk/nltk">source repository</a>. 
Once you've downloaded this, you'll need to run the 
top level setup.py program to install this version of NLTK on your 
machine. 
</blockquote>
<li><b>How can I find out where NLTK is installed on my system?</b> </li><blockquote>Do the following in a Python interpreter session:
<pre><span>&gt;&gt;&gt;</span><span> </span><span>import</span><span> nltk<br /></span><span>&gt;&gt;&gt;</span><span> nltk</span><span>.</span><span>__path__<br /></span><span>[</span><span>'/opt/local/Library/Frameworks/Python.framework/Versions/3.2/lib/python3.2/site-packages/nltk-3.0a3-py3.2.egg/nltk'</span><span>]</span></pre></blockquote>
<li><b>What papers have been published about NLTK?</b> </li><blockquote>NLTK has been used in a wide variety of published research. Please search <a href="https://scholar.google.com.au/scholar?q=%22natural+language+toolkit%22">Google Scholar</a> for details.
</blockquote>
<li><b>How is NLTK development supported?</b> </li><blockquote>NLTK is an open source project that depends mainly on the efforts of volunteers.  Occasionally we have funds for a summer intern or TA to work on specified projects.  Students and teachers also donate code.  In 2008, we received support from <i>Google 
Summer of Code</i>.  We encourage volunteers to get involved (please consult the <a href="https://github.com/nltk/nltk/wiki">wiki</a>). 
If you find the toolkit useful, please make a donation to support further development. 
</blockquote>
<li><b>How did NLTK start?</b> </li><blockquote>The NLTK project began when Steven Bird was teaching CIS-530 at 
the University of Pennsylvania in 2001, and hired his star 
student, Edward Loper, from the previous offering of the course to 
be the teaching assistant (TA).  They agreed a plan for developing 
software infrastructure for NLP teaching that could be easily 
maintained over time.  Edward wrote up 
<a href="http://code.google.com/p/nltk/source/browse/trunk/nltk-old/doc/technical/proposal/proposal.tex" rel="nofollow">the plan</a>, 
and both began work on it right away.  Here is the 
<a href="http://sourceforge.net/mailarchive/forum.php?thread_id=22772&amp;amp;forum_id=960" rel="nofollow">Version 0.2 release announcement</a> 
that appeared in September 2001. 
</blockquote>
<li><b>If I just "use" NLTK using import statements in Python, am I obliged to publish my source code as well?</b> </li><blockquote>No, there is no such obligation.  You can use and modify NLTK without making any code available (see question 1).</blockquote>
<li><b>What is Natural Language Processing?</b> </li><blockquote>Please see our <a href="http://nltk.org/book/">book</a>, or <a href="http://en.wikipedia.org/wiki/Natural_language_processing" rel="nofollow">http://en.wikipedia.org/wiki/Natural_language_processing</a>
</blockquote></ol>