Download Link: https://assignmentchef.com/product/solved-comp9044-test-3-finding-the-most-common-first-name
<br>
<h1>Finding the Most Common First Name</h1>

We need to know the most common first name for each year’s COMP[29]041 students.

We have enrollment data in this format:

$ <strong>wget </strong><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/first_name/files.ln/enrollments.txt"><strong>htt</strong></a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/first_name/files.ln/enrollments.txt"><strong>p</strong></a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/first_name/files.ln/enrollments.txt"><strong>s://c</strong></a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/first_name/files.ln/enrollments.txt"><strong>g</strong></a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/first_name/files.ln/enrollments.txt"><strong>i.cse.unsw.edu.au/~cs2041/20T2/activities/first_name/files.ln/enrollments.txt</strong></a> $ <strong>head enrollments.txt</strong>

COMP1511|5013566|Xin, Mackenzie Darren                             |3648/2|COMPI1 MTRNAH|071.800|18s2|19910428|M

COMP9902|5079970|Park, Xue Hannah Vanessa                          |8543  |ELECAH       |079.333|18s2|19900209|F

COMP1511|5059072|Chung, Michael Jia Tianyu                         |3778/1|COMPCS       |057.250|18s2|19990801|M

COMP1521|5060774|Lim, Stephanie Lauren                             |3785/1|COMPA1       |000.000|18s2|19890113|F

COMP1531|5060774|Lim, Stephanie Lauren                             |3785/1|COMPA1       |000.000|18s2|19890113|F

COMP2521|5060774|Lim, Stephanie Lauren                             |3785/1|COMPA1       |000.000|18s2|19890113|F

COMP9020|5060538|Bi, Samuel Shiyu                                  |6021  |COMPA1       |078.125|18s2|19911004|M

COMP9021|5060538|Bi, Samuel Shiyu                                  |6021  |COMPA1       |078.125|18s2|19911004|M

COMP9902|5072116|Hu, Kai Zhi Patrick                               |3707/1|SENGAH       |070.750|18s2|19930424|M

COMP1511|5036926|Fang, Rebecca Lauren                              |8543  |COMPCS       |000.000|18s2|20000921|F

Write a shell script first_name.sh which takes the name of a file as a command-line argument, The file will contain enrolment data in the above format. first_name.sh should print a single line of output. This line should contain only the most common first name for COMP[29]041 students in the enrollment data. For example:

$ <strong>./first_name.sh enrollments.txt</strong> Vanessa

You can assume there will not be multiple first names which are equally common.

You can assume the data will be correctly formatted No error checking is necessary.

When you think your program is working you can autotest to run some simple automated tests:

$ <strong>2041 autotest first_name</strong>

When you are finished working on this exercise you must submit your work by running give:

$ <strong>give cs2041 test03_first_name first_name.c</strong>

Our new web server requires all HTML files have the suffix .html. Unfortunately we have many HTML files named with the suffix

.htm.

Write a shell script htm2html.sh which changes the name of all files with the suffix .htm in the current directory to have the suffix .html. For example:

<table width="961">

 <tbody>

  <tr>

   <td width="961">$ <strong>touch index.htm small.htm large.htm</strong>$ <strong>ls *.htm*</strong> index.htm  large.htm  small.htm$ <strong>./htm2html.sh</strong> $ <strong>ls *.htm*</strong> index.html  large.html  small.html</td>

  </tr>

 </tbody>

</table>

Your script should stop with EXACTLY the error message shown below and exit status <sub>1</sub> if the .html file already exists. For example:

<table width="961">

 <tbody>

  <tr>

   <td width="961">$ <strong>touch andrew.htm andrew.html</strong>$ <strong>./htm2html.sh </strong> andrew.html exists</td>

  </tr>

 </tbody>

</table>

You can assume the current directory contains at last one .htm file No error checking other then described above is necessary.

When you think your program is working you can autotest to run some simple automated tests:

$ <strong>2041 autotest htm2html</strong>

When you are finished working on this exercise you must submit your work by running give:

$ <strong>give cs2041 test03_htm2html htm2html.sh</strong>

We need check a large number of C programs for missing include files.

Write a shell script missing_include.sh which is give one of more filenames as argument. The files will contain C code. missing_include.sh should print a message if any file included by the C program is not present in the current directory.

Reminder C include lines are of this form:

#include “file.h”

For example:

<table width="961">

 <tbody>

  <tr>

   <td width="961">$ <strong>wget </strong><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/missing_include/file.cp/c_files.zip"><strong>htt</strong></a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/missing_include/file.cp/c_files.zip"><strong>p</strong></a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/missing_include/file.cp/c_files.zip"><strong>s://c</strong></a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/missing_include/file.cp/c_files.zip"><strong>g</strong></a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/missing_include/file.cp/c_files.zip"><strong>i.cse.unsw.edu.au/~cs2041/20T2/activities/missin</strong></a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/missing_include/file.cp/c_files.zip"><strong>g</strong></a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/missing_include/file.cp/c_files.zip"><strong>_include/file.c</strong></a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/missing_include/file.cp/c_files.zip"><strong>p</strong></a><a href="https://cgi.cse.unsw.edu.au/~cs2041/20T2/activities/missing_include/file.cp/c_files.zip"><strong>/c_files.zip</strong></a>$ <strong>unzip c_files.zip</strong> Archive:  c_files.zip   inflating: a.c   inflating: b.c  extracting: b.h  extracting: d.h$ <strong>ls *.[ch]</strong>a.c  a.h  b.c  c.h $ <strong>cat a.c</strong>#include &lt;stdio.h&gt;#include “a.h”#include “b.h” #include “input.h”int a(void){     return 42;}$ <strong>cat b.c</strong>#include &lt;stdio.h&gt;#include “b.h”#include “c.h”#include “d.h” #include &lt;string.h&gt;int b(void){     return b.c;}$ <strong>./missing_include.sh a.c</strong>b.h included into a.c does not exist input.h included into a.c does not exist$ <strong>./missing_include.sh b.c</strong>b.h included into b.c does not existd.h included into b.c does not exist$ <strong>./missing_include.sh a.c b.c</strong>b.h included into a.c does not exist input.h included into a.c does not existb.h included into b.c does not existd.h included into b.c does not exist</td>

  </tr>

 </tbody>

</table>

You can assume filenames do not contain spaces.

You do not have to check files for the C library with angle brackets (&lt;&gt;). For example you do not have to check this line:

#include &lt;stdio.h&gt;

No error checking is necessary.

When you think your program is working you can autotest to run some simple automated tests:

$ <strong>2041 autotest missing_include</strong>

When you are finished working on this exercise you must submit your work by running give:

$ <strong>give cs2041 test03_missing_include missing_include.sh</strong>