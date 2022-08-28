From: <Saved by Blink>
Snapshot-Content-Location: https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-DB0201EN-SkillsNetwork/labs/MySQL/week6/views.md.html
Subject: 
Date: Sun, 28 Aug 2022 17:34:10 -0000
MIME-Version: 1.0
Content-Type: multipart/related;
	type="text/html";
	boundary="----MultipartBoundary--ZeJbom7ua2thyClsILZ3bxA8NwD3gXWgKq2ZLWICWB----"


------MultipartBoundary--ZeJbom7ua2thyClsILZ3bxA8NwD3gXWgKq2ZLWICWB----
Content-Type: text/html
Content-ID: <frame-C9119762F8FF74C9E803D85CA9C38F5C@mhtml.blink>
Content-Transfer-Encoding: quoted-printable
Content-Location: https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-DB0201EN-SkillsNetwork/labs/MySQL/week6/views.md.html

<!DOCTYPE html><html lang=3D"en"><head><meta http-equiv=3D"Content-Type" co=
ntent=3D"text/html; charset=3DUTF-8"><link rel=3D"stylesheet" type=3D"text/=
css" href=3D"cid:css-0b9a2b48-0097-44d2-a577-f16bc8f7f56d@mhtml.blink" /><l=
ink rel=3D"stylesheet" type=3D"text/css" href=3D"cid:css-44594ecf-dceb-4068=
-87be-4c58d7b160e4@mhtml.blink" />
   =20
    <meta name=3D"viewport" content=3D"width=3Ddevice-width, initial-scale=
=3D1">
    <link rel=3D"stylesheet" href=3D"https://stackpath.bootstrapcdn.com/boo=
tstrap/4.3.1/css/bootstrap.min.css" crossorigin=3D"anonymous">
    <link rel=3D"stylesheet" href=3D"https://unpkg.com/@highlightjs/cdn-ass=
ets@10.7.1/styles/default.min.css">
  </head>
  <body>
    <img src=3D"https://cf-courses-data.s3.us.cloud-object-storage.appdomai=
n.cloud/IBMDeveloperSkillsNetwork-DB0201EN-SkillsNetwork/labs/MySQL/week6/i=
mages/IDSNlogo.png" width=3D"200" height=3D"200">
    <h1>Hands-on Lab: Using Views in MySQL using phpMyAdmin</h1>
    <p><strong>Estimated time needed:</strong> 20 minutes</p>
    <p>In this lab, you will learn how to create tables and load data in th=
e MySQL database service using the phpMyAdmin graphical user interface (GUI=
) tool.</p>
    <h1></h1>
    <h2>Software Used in this Lab</h2>
    <p>In this lab, you will use <a href=3D"https://www.mysql.com/?utm_medi=
um=3DExinfluencer&amp;utm_source=3DExinfluencer&amp;utm_content=3D000026UJ&=
amp;utm_term=3D10006555&amp;utm_id=3DNA-SkillsNetwork-Channel-SkillsNetwork=
CoursesIBMDB0110ENSkillsNetwork24601058-2021-01-01">MySQL</a>. MySQL is a R=
elational Database Management System (RDBMS) designed to efficiently store,=
 manipulate, and retrieve data.</p>
    <img src=3D"https://cf-courses-data.s3.us.cloud-object-storage.appdomai=
n.cloud/IBM-DB0110EN-SkillsNetwork/labs/Lab%20-%20Create%20Tables%20and%20L=
oad%20Data%20in%20MySQL%20using%20phpMyAdmin/images/mysql.png" width=3D"100=
" height=3D"100">
    <p></p>
    <p>To complete this lab you will utilize MySQL relational database serv=
ice available as part of IBM Skills Network Labs (SN Labs) Cloud IDE. SN La=
bs is a virtual lab environment used in this course.</p>
    <h1></h1>
    <h2>Database Used in this Lab</h2>
    <p>The database used in this lab is an internal database. You will be w=
orking on a sample HR database. This HR database schema consists of 5 table=
s called <strong>EMPLOYEES</strong>, <strong>JOB_HISTORY</strong>, <strong>=
JOBS</strong>, <strong>DEPARTMENTS</strong> and <strong>LOCATIONS</strong>.=
 Each table has a few rows of sample data. The following diagram shows the =
tables for the HR database:</p>
    <img src=3D"https://cf-courses-data.s3.us.cloud-object-storage.appdomai=
n.cloud/IBMDeveloperSkillsNetwork-DB0201EN-SkillsNetwork/labs/Labs_Coursera=
_V5/labs/Lab%20-%20Create%20tables%20using%20SQL%20scripts%20and%20Load%20d=
ata%20into%20tables/images/Sample_1.PNG" width=3D"670" height=3D"400">
    <h2>Objectives</h2>
    <p>After completing this lab, you will be able to:</p>
    <ul>
      <li>Create a View and show a selection of data for a given table</li>
      <li>Update a View to combine two or more tables in meaningful ways</l=
i>
      <li>Drop a created View</li>
    </ul>
    <p>In this lab, you will learn about using views. In SQL, a view is an =
alternative way of representing data that exists in one or more tables. Jus=
t like a real table, it contains rows and columns. The fields in a view are=
 fields from one or more real tables in the database. Though views can be q=
ueried like a table, views are dynamic; only the definition of the view is =
stored, not the data.</p><br>
    <p><strong>How does the syntax of a CREATE VIEW statement look?</strong=
></p>
    <pre class=3D"code-badge-pre"><div class=3D"code-badge">
        <div class=3D"code-badge-language">pgsql</div>
        <div title=3D"Copy to clipboard">
            <i class=3D"code-badge-copy-icon code-badge-copy-icon"></i>
        </div>
     </div><code class=3D"hljs language-pgsql"><span class=3D"hljs-keyword"=
>CREATE</span> <span class=3D"hljs-keyword">VIEW</span> view_name <span cla=
ss=3D"hljs-keyword">AS</span>
<span class=3D"hljs-keyword">SELECT</span> column1, column2, ...
<span class=3D"hljs-keyword">FROM</span> <span class=3D"hljs-built_in">tabl=
e_name</span>
<span class=3D"hljs-keyword">WHERE</span> condition;
</code></pre><br>
    <p><strong>How does the syntax of a REPLACE VIEW statement look?</stron=
g></p>
    <pre class=3D"code-badge-pre"><div class=3D"code-badge">
        <div class=3D"code-badge-language">pgsql</div>
        <div title=3D"Copy to clipboard">
            <i class=3D"code-badge-copy-icon code-badge-copy-icon"></i>
        </div>
     </div><code class=3D"hljs language-pgsql"><span class=3D"hljs-keyword"=
>CREATE</span> <span class=3D"hljs-keyword">OR REPLACE</span> <span class=
=3D"hljs-keyword">VIEW</span> view_name <span class=3D"hljs-keyword">AS</sp=
an>
<span class=3D"hljs-keyword">SELECT</span> column1, column2, ...
<span class=3D"hljs-keyword">FROM</span> <span class=3D"hljs-built_in">tabl=
e_name</span>
<span class=3D"hljs-keyword">WHERE</span> condition;
</code></pre><br>
    <p><strong>How does the syntax of a DROP VIEW statement look?</strong><=
/p>
    <pre class=3D"code-badge-pre"><div class=3D"code-badge">
        <div class=3D"code-badge-language">gauss</div>
        <div title=3D"Copy to clipboard">
            <i class=3D"code-badge-copy-icon code-badge-copy-icon"></i>
        </div>
     </div><code class=3D"hljs language-gauss"><span class=3D"hljs-built_in=
">DROP</span> <span class=3D"hljs-built_in">VIEW</span> view_name;
</code></pre><br>
    <h1>Exercise 1: Create a View</h1>
    <p>In this exercise, you will create a View and show a selection of dat=
a for a given table.</p>
    <ol>
      <li>
        <p>Let's create a view called <strong>EMPSALARY</strong> to display=
 salary along with some basic sensitive data of employees from the HR datab=
ase. To create the <strong>EMPSALARY</strong> view from the <strong>EMPLOYE=
ES</strong> table, Copy the code below and paste it to the textarea of the =
<strong>SQL</strong> page. Click <strong>Go</strong>.</p>
        <pre class=3D"code-badge-pre"><div class=3D"code-badge">
        <div class=3D"code-badge-language">n1ql</div>
        <div title=3D"Copy to clipboard">
            <i class=3D"code-badge-copy-icon code-badge-copy-icon"></i>
        </div>
     </div><code class=3D"hljs language-n1ql"><span class=3D"hljs-keyword">=
CREATE</span> <span class=3D"hljs-keyword">VIEW</span> EMPSALARY <span clas=
s=3D"hljs-keyword">AS</span>=20
<span class=3D"hljs-keyword">SELECT</span> EMP_ID, F_NAME, L_NAME, B_DATE, =
SEX, SALARY
<span class=3D"hljs-keyword">FROM</span> EMPLOYEES;=20
</code></pre>
        <img src=3D"https://cf-courses-data.s3.us.cloud-object-storage.appd=
omain.cloud/IBMDeveloperSkillsNetwork-DB0201EN-SkillsNetwork/labs/MySQL/wee=
k6/images/1.1.png" width=3D"1060" height=3D"150">
        <p></p>
      </li>
      <li>
        <p>Using SELECT, query the <strong>EMPSALARY</strong> view to retri=
eve all the records.Copy the code below and paste it to the textarea of the=
 <strong>SQL</strong> page. Click <strong>Go</strong>.</p>
        <pre class=3D"code-badge-pre"><div class=3D"code-badge">
        <div class=3D"code-badge-language">n1ql</div>
        <div title=3D"Copy to clipboard">
            <i class=3D"code-badge-copy-icon code-badge-copy-icon"></i>
        </div>
     </div><code class=3D"hljs language-n1ql"><span class=3D"hljs-keyword">=
SELECT</span> * <span class=3D"hljs-keyword">FROM</span> EMPSALARY;
</code></pre>
        <img src=3D"https://cf-courses-data.s3.us.cloud-object-storage.appd=
omain.cloud/IBMDeveloperSkillsNetwork-DB0201EN-SkillsNetwork/labs/MySQL/wee=
k6/images/1.2.png" width=3D"1100" height=3D"500">
      </li>
    </ol>
    <h1>Exercise 2: Update a View</h1>
    <p>In this exercise, you will update a View to combine two or more tabl=
es in meaningful ways.</p>
    <ol>
      <li>
        <p>It now seems that the <strong>EMPSALARY</strong> view we created=
 in exercise 1 doesn't contain enough salary information, such as max/min s=
alary and the job title of the employees. Let's update the <strong>EMPSALAR=
Y</strong> view:</p>
        <ul>
          <li>combining two tables <strong>EMPLOYEES</strong> and <strong>J=
OBS</strong> so that we can display our desired information from the HR dat=
abase.</li>
          <li>including the columns <strong>JOB_TITLE, MIN_SALARY, MAX_SALA=
RY</strong> of the <strong>JOBS</strong> table as well as excluding the <st=
rong>SALARY</strong> column of the <strong>EMPLOYEES</strong> table.</li>
        </ul>
        <p></p>
        <p>Copy the code below and paste it to the textarea of the <strong>=
SQL</strong> page. Click <strong>Go</strong>..</p>
        <pre class=3D"code-badge-pre"><div class=3D"code-badge">
        <div class=3D"code-badge-language">n1ql</div>
        <div title=3D"Copy to clipboard">
            <i class=3D"code-badge-copy-icon code-badge-copy-icon"></i>
        </div>
     </div><code class=3D"hljs language-n1ql"><span class=3D"hljs-keyword">=
CREATE</span> <span class=3D"hljs-keyword">OR</span> <span class=3D"hljs-bu=
ilt_in">REPLACE</span> <span class=3D"hljs-keyword">VIEW</span> EMPSALARY  =
<span class=3D"hljs-keyword">AS</span>=20
<span class=3D"hljs-keyword">SELECT</span> EMP_ID, F_NAME, L_NAME, B_DATE, =
SEX, JOB_TITLE, MIN_SALARY, MAX_SALARY
<span class=3D"hljs-keyword">FROM</span> EMPLOYEES, JOBS
<span class=3D"hljs-keyword">WHERE</span> EMPLOYEES.JOB_ID =3D JOBS.JOB_IDE=
NT;
</code></pre>
        <blockquote>
          <p><strong>NOTE:</strong> Don't worry if you don't understand how=
 to combine to two tables using implicit inner join. You will learn more ab=
out joins later on. For now, just think you are combining the data of two d=
ifferent tables, <strong>EMPLOYEES</strong> and <strong>JOBS</strong> by co=
nnecting their respective columns <strong>JOB_ID</strong> and <strong>JOB_I=
DENT</strong> since both the columns contain common unique data. You can ha=
ve a look at the diagram (at the beginning of the lab) showing the tables f=
or the HR database to observe how the <strong>JOB_ID</strong> and <strong>J=
OB_IDENT</strong> columns from the <strong>EMPLOYEES</strong> and <strong>J=
OBS</strong> tables respectively contain common unique data.</p>
        </blockquote>
        <img src=3D"https://cf-courses-data.s3.us.cloud-object-storage.appd=
omain.cloud/IBMDeveloperSkillsNetwork-DB0201EN-SkillsNetwork/labs/MySQL/wee=
k6/images/2.1.png" width=3D"1120" height=3D"150">
        <p></p>
      </li>
      <li>
        <p>Using SELECT, query the updated <strong>EMPSALARY</strong> view =
to retrieve all the records. Copy the code below and paste it to the textar=
ea of the <strong>SQL</strong> page. Click <strong>Go</strong>.</p>
        <pre class=3D"code-badge-pre"><div class=3D"code-badge">
        <div class=3D"code-badge-language">n1ql</div>
        <div title=3D"Copy to clipboard">
            <i class=3D"code-badge-copy-icon code-badge-copy-icon"></i>
        </div>
     </div><code class=3D"hljs language-n1ql"><span class=3D"hljs-keyword">=
SELECT</span> * <span class=3D"hljs-keyword">FROM</span> EMPSALARY;
</code></pre>
      </li>
    </ol>
    <p>
      <img src=3D"https://cf-courses-data.s3.us.cloud-object-storage.appdom=
ain.cloud/IBMDeveloperSkillsNetwork-DB0201EN-SkillsNetwork/labs/MySQL/week6=
/images/2.2.png" alt=3D"image">
    </p>
    <h1>Exercise 3: Drop a View</h1>
    <p>In this exercise, you will drop a created View.</p>
    <ol>
      <li>
        <p>Let's delete the created <strong>EMPSALARY</strong> view. Copy t=
he code below and paste it to the paste it to the textarea of the <strong>S=
QL</strong> page. Click <strong>Go</strong>..</p>
        <pre class=3D"code-badge-pre"><div class=3D"code-badge">
        <div class=3D"code-badge-language">gauss</div>
        <div title=3D"Copy to clipboard">
            <i class=3D"code-badge-copy-icon code-badge-copy-icon"></i>
        </div>
     </div><code class=3D"hljs language-gauss"><span class=3D"hljs-built_in=
">DROP</span> <span class=3D"hljs-built_in">VIEW</span> EMPSALARY;
</code></pre>
        <img src=3D"https://cf-courses-data.s3.us.cloud-object-storage.appd=
omain.cloud/IBMDeveloperSkillsNetwork-DB0201EN-SkillsNetwork/labs/MySQL/wee=
k6/images/3.1.png" width=3D"980" height=3D"150">
        <p></p>
      </li>
      <li>
        <p>Using SELECT, you can verify whether the <strong>EMPSALARY</stro=
ng> view has been deleted or not. Copy the code below and paste it to the t=
extarea of the <strong>SQL</strong> page. Click <strong>Go</strong>..</p>
        <pre class=3D"code-badge-pre"><div class=3D"code-badge">
        <div class=3D"code-badge-language">n1ql</div>
        <div title=3D"Copy to clipboard">
            <i class=3D"code-badge-copy-icon code-badge-copy-icon"></i>
        </div>
     </div><code class=3D"hljs language-n1ql"><span class=3D"hljs-keyword">=
SELECT</span> * <span class=3D"hljs-keyword">FROM</span> EMPSALARY;
</code></pre>
        <img src=3D"https://cf-courses-data.s3.us.cloud-object-storage.appd=
omain.cloud/IBMDeveloperSkillsNetwork-DB0201EN-SkillsNetwork/labs/MySQL/wee=
k6/images/3.2.png" width=3D"1055" height=3D"250">
      </li>
    </ol><br>
    <h3>Congratulations! You have completed this lab, and you are ready for=
 the next topic.</h3>
    <h3><br></h3>
    <h1>Author(s)</h1>
    <p><a href=3D"https://www.linkedin.com/in/lakshmi-holla-b39062149/?utm_=
medium=3DExinfluencer&amp;utm_source=3DExinfluencer&amp;utm_content=3D00002=
6UJ&amp;utm_term=3D10006555&amp;utm_id=3DNA-SkillsNetwork-Channel-SkillsNet=
workCoursesIBMDeveloperSkillsNetworkDB0201ENSkillsNetwork20127838-2022-01-0=
1" target=3D"_blank" rel=3D"external">Lakshmi Holla</a></p>
    <p><a href=3D"https://www.linkedin.com/in/malika-goyal-04798622/?utm_me=
dium=3DExinfluencer&amp;utm_source=3DExinfluencer&amp;utm_content=3D000026U=
J&amp;utm_term=3D10006555&amp;utm_id=3DNA-SkillsNetwork-Channel-SkillsNetwo=
rkCoursesIBMDeveloperSkillsNetworkDB0201ENSkillsNetwork20127838-2022-01-01"=
 target=3D"_blank" rel=3D"external">Malika Singla</a></p>
    <h2>Changelog</h2>
    <table>
      <thead>
        <tr>
          <th>Date</th>
          <th>Version</th>
          <th>Changed by</th>
          <th>Change Description</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>2021-11-01</td>
          <td>0.1</td>
          <td>Lakshmi Holla, Malika Singla</td>
          <td>Initial Version</td>
        </tr>
      </tbody>
    </table>
    <h2></h2>
    <h3 align=3D"center">=C2=A9 IBM Corporation 2021. All rights reserved.<=
/h3>
    <h3></h3>
   =20
   =20
   =20
   =20
 =20

<div id=3D"CodeBadgeTemplate" style=3D"display:none">
    <div class=3D"code-badge">
        <div class=3D"code-badge-language">{{language}}</div>
        <div title=3D"Copy to clipboard">
            <i class=3D"{{copyIconClass}} code-badge-copy-icon"></i>
        </div>
     </div>
</div><iframe frameborder=3D"0" scrolling=3D"no" style=3D"background-color:=
 transparent; border: 0px; display: none;"></iframe><div id=3D"GOOGLE_INPUT=
_CHEXT_FLAG" input=3D"" input_stat=3D"{&quot;tlang&quot;:true,&quot;tsbc&qu=
ot;:true,&quot;pun&quot;:true,&quot;mk&quot;:true,&quot;ss&quot;:true}" sty=
le=3D"display: none;"></div></body></html>
------MultipartBoundary--ZeJbom7ua2thyClsILZ3bxA8NwD3gXWgKq2ZLWICWB----
Content-Type: text/css
Content-Transfer-Encoding: quoted-printable
Content-Location: cid:css-0b9a2b48-0097-44d2-a577-f16bc8f7f56d@mhtml.blink

@charset "utf-8";

img { max-width: 100%; height: auto; }

body { padding: 10px; margin: 10px; }

table td, table th { padding: 0.75rem; vertical-align: top; border-top: 1px=
 solid rgb(222, 226, 230); }

blockquote { background: rgb(249, 249, 249); border-left: 10px solid rgb(20=
4, 204, 204); margin: 1.5em 10px; padding: 1em 10px 0.1em; quotes: "=E2=80=
=9C" "=E2=80=9D" "=E2=80=98" "=E2=80=99"; }

h1, h2, h3, h4, h5, h6 { font-weight: 500; padding-top: 20px; }

ul > li > ul { padding-bottom: 1rem; }

.code-badge-language { display: none; }

.code-badge-copy-icon { background: url("data:image/svg+xml;base64,PHN2ZyBh=
cmlhLWhpZGRlbj0idHJ1ZSIgZm9jdXNhYmxlPSJmYWxzZSIgZGF0YS1wcmVmaXg9ImZhciIgZGF=
0YS1pY29uPSJjb3B5IiBjbGFzcz0ic3ZnLWlubGluZS0tZmEgZmEtY29weSBmYS13LTE0IiByb2=
xlPSJpbWciIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgdmlld0JveD0iMCAwI=
DQ0OCA1MTIiPjxwYXRoIGZpbGw9ImN1cnJlbnRDb2xvciIgZD0iTTQzMy45NDEgNjUuOTQxbC01=
MS44ODItNTEuODgyQTQ4IDQ4IDAgMCAwIDM0OC4xMTggMEgxNzZjLTI2LjUxIDAtNDggMjEuNDk=
tNDggNDh2NDhINDhjLTI2LjUxIDAtNDggMjEuNDktNDggNDh2MzIwYzAgMjYuNTEgMjEuNDkgND=
ggNDggNDhoMjI0YzI2LjUxIDAgNDgtMjEuNDkgNDgtNDh2LTQ4aDgwYzI2LjUxIDAgNDgtMjEuN=
DkgNDgtNDhWOTkuODgyYTQ4IDQ4IDAgMCAwLTE0LjA1OS0zMy45NDF6TTI2NiA0NjRINTRhNiA2=
IDAgMCAxLTYtNlYxNTBhNiA2IDAgMCAxIDYtNmg3NHYyMjRjMCAyNi41MSAyMS40OSA0OCA0OCA=
0OGg5NnY0MmE2IDYgMCAwIDEtNiA2em0xMjgtOTZIMTgyYTYgNiAwIDAgMS02LTZWNTRhNiA2ID=
AgMCAxIDYtNmgxMDZ2ODhjMCAxMy4yNTUgMTAuNzQ1IDI0IDI0IDI0aDg4djIwMmE2IDYgMCAwI=
DEtNiA2em02LTI1NmgtNjRWNDhoOS42MzJjMS41OTEgMCAzLjExNy42MzIgNC4yNDMgMS43NTds=
NDguMzY4IDQ4LjM2OGE2IDYgMCAwIDEgMS43NTcgNC4yNDNWMTEyeiI+PC9wYXRoPjwvc3ZnPg=
=3D=3D") 0% 0% / 100% 100%; }

.code-badge { bottom: 0px !important; top: unset !important; background: un=
set !important; }

.code-badge > .code-badge-check-icon { background: green; }

.code-badge-check-icon { font-size: 1.2em; cursor: pointer; padding: 0px 7p=
x; background: url("data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3d=
y53My5vcmcvMjAwMC9zdmciIGFyaWEtaGlkZGVuPSJ0cnVlIiBmb2N1c2FibGU9ImZhbHNlIiBk=
YXRhLXByZWZpeD0iZmFzIiBkYXRhLWljb249ImNoZWNrIiBjbGFzcz0ic3ZnLWlubGluZS0tZmE=
gZmEtY2hlY2sgZmEtdy0xNiIgcm9sZT0iaW1nIiB2aWV3Qm94PSIwIDAgNTEyIDUxMiIgc3R5bG=
U9IiYjMTA7ICAgIGNvbG9yOiAjMmFmZjMyOyYjMTA7Ij48cGF0aCBmaWxsPSJjdXJyZW50Q29sb=
3IiIGQ9Ik0xNzMuODk4IDQzOS40MDRsLTE2Ni40LTE2Ni40Yy05Ljk5Ny05Ljk5Ny05Ljk5Ny0y=
Ni4yMDYgMC0zNi4yMDRsMzYuMjAzLTM2LjIwNGM5Ljk5Ny05Ljk5OCAyNi4yMDctOS45OTggMzY=
uMjA0IDBMMTkyIDMxMi42OSA0MzIuMDk1IDcyLjU5NmM5Ljk5Ny05Ljk5NyAyNi4yMDctOS45OT=
cgMzYuMjA0IDBsMzYuMjAzIDM2LjIwNGM5Ljk5NyA5Ljk5NyA5Ljk5NyAyNi4yMDYgMCAzNi4yM=
DRsLTI5NC40IDI5NC40MDFjLTkuOTk4IDkuOTk3LTI2LjIwNyA5Ljk5Ny0zNi4yMDQtLjAwMXoi=
Lz48L3N2Zz4=3D") 0% 0% / 100% 100%; }
------MultipartBoundary--ZeJbom7ua2thyClsILZ3bxA8NwD3gXWgKq2ZLWICWB----
Content-Type: text/css
Content-Transfer-Encoding: quoted-printable
Content-Location: cid:css-44594ecf-dceb-4068-87be-4c58d7b160e4@mhtml.blink

@charset "utf-8";

@media print {
  .code-badge { display: none; }
}

.code-badge-pre { position: relative; }

.code-badge { display: flex; flex-direction: row; white-space: normal; back=
ground: rgb(51, 51, 51); color: white; font-size: 0.875em; opacity: 0.5; tr=
ansition: opacity 0.5s linear 0s; border-radius: 0px 0px 0px 7px; padding: =
5px 8px; position: absolute; right: 0px; top: 0px; }

.code-badge.active { opacity: 0.8; }

.code-badge:hover { opacity: 0.95; }

.code-badge a, .code-badge a:hover { text-decoration: none; }

.code-badge-language { margin-right: 10px; font-weight: 600; color: goldenr=
od; }

.code-badge-copy-icon { font-size: 1.2em; cursor: pointer; padding: 0px 7px=
; }
------MultipartBoundary--ZeJbom7ua2thyClsILZ3bxA8NwD3gXWgKq2ZLWICWB----
Content-Type: text/css
Content-Transfer-Encoding: quoted-printable
Content-Location: https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css

@charset "utf-8";

:root { --blue:#007bff; --indigo:#6610f2; --purple:#6f42c1; --pink:#e83e8c;=
 --red:#dc3545; --orange:#fd7e14; --yellow:#ffc107; --green:#28a745; --teal=
:#20c997; --cyan:#17a2b8; --white:#fff; --gray:#6c757d; --gray-dark:#343a40=
; --primary:#007bff; --secondary:#6c757d; --success:#28a745; --info:#17a2b8=
; --warning:#ffc107; --danger:#dc3545; --light:#f8f9fa; --dark:#343a40; --b=
reakpoint-xs:0; --breakpoint-sm:576px; --breakpoint-md:768px; --breakpoint-=
lg:992px; --breakpoint-xl:1200px; --font-family-sans-serif:-apple-system,Bl=
inkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial,"Noto Sans",sans-=
serif,"Apple Color Emoji","Segoe UI Emoji","Segoe UI Symbol","Noto Color Em=
oji"; --font-family-monospace:SFMono-Regular,Menlo,Monaco,Consolas,"Liberat=
ion Mono","Courier New",monospace; }

*, ::after, ::before { box-sizing: border-box; }

html { font-family: sans-serif; line-height: 1.15; text-size-adjust: 100%; =
-webkit-tap-highlight-color: transparent; }

article, aside, figcaption, figure, footer, header, hgroup, main, nav, sect=
ion { display: block; }

body { margin: 0px; font-family: -apple-system, BlinkMacSystemFont, "Segoe =
UI", Roboto, "Helvetica Neue", Arial, "Noto Sans", sans-serif, "Apple Color=
 Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji"; font-size=
: 1rem; font-weight: 400; line-height: 1.5; color: rgb(33, 37, 41); text-al=
ign: left; background-color: rgb(255, 255, 255); }

[tabindex=3D"-1"]:focus { outline: 0px !important; }

hr { box-sizing: content-box; height: 0px; overflow: visible; }

h1, h2, h3, h4, h5, h6 { margin-top: 0px; margin-bottom: 0.5rem; }

p { margin-top: 0px; margin-bottom: 1rem; }

abbr[data-original-title], abbr[title] { text-decoration: underline dotted;=
 cursor: help; border-bottom: 0px; text-decoration-skip-ink: none; }

address { margin-bottom: 1rem; font-style: normal; line-height: inherit; }

dl, ol, ul { margin-top: 0px; margin-bottom: 1rem; }

ol ol, ol ul, ul ol, ul ul { margin-bottom: 0px; }

dt { font-weight: 700; }

dd { margin-bottom: 0.5rem; margin-left: 0px; }

blockquote { margin: 0px 0px 1rem; }

b, strong { font-weight: bolder; }

small { font-size: 80%; }

sub, sup { position: relative; font-size: 75%; line-height: 0; vertical-ali=
gn: baseline; }

sub { bottom: -0.25em; }

sup { top: -0.5em; }

a { color: rgb(0, 123, 255); text-decoration: none; background-color: trans=
parent; }

a:hover { color: rgb(0, 86, 179); text-decoration: underline; }

a:not([href]):not([tabindex]) { color: inherit; text-decoration: none; }

a:not([href]):not([tabindex]):focus, a:not([href]):not([tabindex]):hover { =
color: inherit; text-decoration: none; }

a:not([href]):not([tabindex]):focus { outline: 0px; }

code, kbd, pre, samp { font-family: SFMono-Regular, Menlo, Monaco, Consolas=
, "Liberation Mono", "Courier New", monospace; font-size: 1em; }

pre { margin-top: 0px; margin-bottom: 1rem; overflow: auto; }

figure { margin: 0px 0px 1rem; }

img { vertical-align: middle; border-style: none; }

svg { overflow: hidden; vertical-align: middle; }

table { border-collapse: collapse; }

caption { padding-top: 0.75rem; padding-bottom: 0.75rem; color: rgb(108, 11=
7, 125); text-align: left; caption-side: bottom; }

th { text-align: inherit; }

label { display: inline-block; margin-bottom: 0.5rem; }

button { border-radius: 0px; }

button:focus { outline: -webkit-focus-ring-color auto 5px; }

button, input, optgroup, select, textarea { margin: 0px; font-family: inher=
it; font-size: inherit; line-height: inherit; }

button, input { overflow: visible; }

button, select { text-transform: none; }

select { overflow-wrap: normal; }

[type=3D"button"], [type=3D"reset"], [type=3D"submit"], button { appearance=
: button; }

[type=3D"button"]:not(:disabled), [type=3D"reset"]:not(:disabled), [type=3D=
"submit"]:not(:disabled), button:not(:disabled) { cursor: pointer; }

input[type=3D"checkbox"], input[type=3D"radio"] { box-sizing: border-box; p=
adding: 0px; }

input[type=3D"date"], input[type=3D"datetime-local"], input[type=3D"month"]=
, input[type=3D"time"] { appearance: listbox; }

textarea { overflow: auto; resize: vertical; }

fieldset { min-width: 0px; padding: 0px; margin: 0px; border: 0px; }

legend { display: block; width: 100%; max-width: 100%; padding: 0px; margin=
-bottom: 0.5rem; font-size: 1.5rem; line-height: inherit; color: inherit; w=
hite-space: normal; }

progress { vertical-align: baseline; }

[type=3D"number"]::-webkit-inner-spin-button, [type=3D"number"]::-webkit-ou=
ter-spin-button { height: auto; }

[type=3D"search"] { outline-offset: -2px; appearance: none; }

[type=3D"search"]::-webkit-search-decoration { appearance: none; }

::-webkit-file-upload-button { font: inherit; appearance: button; }

output { display: inline-block; }

summary { display: list-item; cursor: pointer; }

template { display: none; }

[hidden] { display: none !important; }

.h1, .h2, .h3, .h4, .h5, .h6, h1, h2, h3, h4, h5, h6 { margin-bottom: 0.5re=
m; font-weight: 500; line-height: 1.2; }

.h1, h1 { font-size: 2.5rem; }

.h2, h2 { font-size: 2rem; }

.h3, h3 { font-size: 1.75rem; }

.h4, h4 { font-size: 1.5rem; }

.h5, h5 { font-size: 1.25rem; }

.h6, h6 { font-size: 1rem; }

.lead { font-size: 1.25rem; font-weight: 300; }

.display-1 { font-size: 6rem; font-weight: 300; line-height: 1.2; }

.display-2 { font-size: 5.5rem; font-weight: 300; line-height: 1.2; }

.display-3 { font-size: 4.5rem; font-weight: 300; line-height: 1.2; }

.display-4 { font-size: 3.5rem; font-weight: 300; line-height: 1.2; }

hr { margin-top: 1rem; margin-bottom: 1rem; border-width: 1px 0px 0px; bord=
er-right-style: initial; border-bottom-style: initial; border-left-style: i=
nitial; border-right-color: initial; border-bottom-color: initial; border-l=
eft-color: initial; border-image: initial; border-top-style: solid; border-=
top-color: rgba(0, 0, 0, 0.1); }

.small, small { font-size: 80%; font-weight: 400; }

.mark, mark { padding: 0.2em; background-color: rgb(252, 248, 227); }

.list-unstyled { padding-left: 0px; list-style: none; }

.list-inline { padding-left: 0px; list-style: none; }

.list-inline-item { display: inline-block; }

.list-inline-item:not(:last-child) { margin-right: 0.5rem; }

.initialism { font-size: 90%; text-transform: uppercase; }

.blockquote { margin-bottom: 1rem; font-size: 1.25rem; }

.blockquote-footer { display: block; font-size: 80%; color: rgb(108, 117, 1=
25); }

.blockquote-footer::before { content: "=E2=80=94=C2=A0"; }

.img-fluid { max-width: 100%; height: auto; }

.img-thumbnail { padding: 0.25rem; background-color: rgb(255, 255, 255); bo=
rder: 1px solid rgb(222, 226, 230); border-radius: 0.25rem; max-width: 100%=
; height: auto; }

.figure { display: inline-block; }

.figure-img { margin-bottom: 0.5rem; line-height: 1; }

.figure-caption { font-size: 90%; color: rgb(108, 117, 125); }

code { font-size: 87.5%; color: rgb(232, 62, 140); word-break: break-word; =
}

a > code { color: inherit; }

kbd { padding: 0.2rem 0.4rem; font-size: 87.5%; color: rgb(255, 255, 255); =
background-color: rgb(33, 37, 41); border-radius: 0.2rem; }

kbd kbd { padding: 0px; font-size: 100%; font-weight: 700; }

pre { display: block; font-size: 87.5%; color: rgb(33, 37, 41); }

pre code { font-size: inherit; color: inherit; word-break: normal; }

.pre-scrollable { max-height: 340px; overflow-y: scroll; }

.container { width: 100%; padding-right: 15px; padding-left: 15px; margin-r=
ight: auto; margin-left: auto; }

@media (min-width: 576px) {
  .container { max-width: 540px; }
}

@media (min-width: 768px) {
  .container { max-width: 720px; }
}

@media (min-width: 992px) {
  .container { max-width: 960px; }
}

@media (min-width: 1200px) {
  .container { max-width: 1140px; }
}

.container-fluid { width: 100%; padding-right: 15px; padding-left: 15px; ma=
rgin-right: auto; margin-left: auto; }

.row { display: flex; flex-wrap: wrap; margin-right: -15px; margin-left: -1=
5px; }

.no-gutters { margin-right: 0px; margin-left: 0px; }

.no-gutters > .col, .no-gutters > [class*=3D"col-"] { padding-right: 0px; p=
adding-left: 0px; }

.col, .col-1, .col-10, .col-11, .col-12, .col-2, .col-3, .col-4, .col-5, .c=
ol-6, .col-7, .col-8, .col-9, .col-auto, .col-lg, .col-lg-1, .col-lg-10, .c=
ol-lg-11, .col-lg-12, .col-lg-2, .col-lg-3, .col-lg-4, .col-lg-5, .col-lg-6=
, .col-lg-7, .col-lg-8, .col-lg-9, .col-lg-auto, .col-md, .col-md-1, .col-m=
d-10, .col-md-11, .col-md-12, .col-md-2, .col-md-3, .col-md-4, .col-md-5, .=
col-md-6, .col-md-7, .col-md-8, .col-md-9, .col-md-auto, .col-sm, .col-sm-1=
, .col-sm-10, .col-sm-11, .col-sm-12, .col-sm-2, .col-sm-3, .col-sm-4, .col=
-sm-5, .col-sm-6, .col-sm-7, .col-sm-8, .col-sm-9, .col-sm-auto, .col-xl, .=
col-xl-1, .col-xl-10, .col-xl-11, .col-xl-12, .col-xl-2, .col-xl-3, .col-xl=
-4, .col-xl-5, .col-xl-6, .col-xl-7, .col-xl-8, .col-xl-9, .col-xl-auto { p=
osition: relative; width: 100%; padding-right: 15px; padding-left: 15px; }

.col { flex-basis: 0px; flex-grow: 1; max-width: 100%; }

.col-auto { flex: 0 0 auto; width: auto; max-width: 100%; }

.col-1 { flex: 0 0 8.33333%; max-width: 8.33333%; }

.col-2 { flex: 0 0 16.6667%; max-width: 16.6667%; }

.col-3 { flex: 0 0 25%; max-width: 25%; }

.col-4 { flex: 0 0 33.3333%; max-width: 33.3333%; }

.col-5 { flex: 0 0 41.6667%; max-width: 41.6667%; }

.col-6 { flex: 0 0 50%; max-width: 50%; }

.col-7 { flex: 0 0 58.3333%; max-width: 58.3333%; }

.col-8 { flex: 0 0 66.6667%; max-width: 66.6667%; }

.col-9 { flex: 0 0 75%; max-width: 75%; }

.col-10 { flex: 0 0 83.3333%; max-width: 83.3333%; }

.col-11 { flex: 0 0 91.6667%; max-width: 91.6667%; }

.col-12 { flex: 0 0 100%; max-width: 100%; }

.order-first { order: -1; }

.order-last { order: 13; }

.order-0 { order: 0; }

.order-1 { order: 1; }

.order-2 { order: 2; }

.order-3 { order: 3; }

.order-4 { order: 4; }

.order-5 { order: 5; }

.order-6 { order: 6; }

.order-7 { order: 7; }

.order-8 { order: 8; }

.order-9 { order: 9; }

.order-10 { order: 10; }

.order-11 { order: 11; }

.order-12 { order: 12; }

.offset-1 { margin-left: 8.33333%; }

.offset-2 { margin-left: 16.6667%; }

.offset-3 { margin-left: 25%; }

.offset-4 { margin-left: 33.3333%; }

.offset-5 { margin-left: 41.6667%; }

.offset-6 { margin-left: 50%; }

.offset-7 { margin-left: 58.3333%; }

.offset-8 { margin-left: 66.6667%; }

.offset-9 { margin-left: 75%; }

.offset-10 { margin-left: 83.3333%; }

.offset-11 { margin-left: 91.6667%; }

@media (min-width: 576px) {
  .col-sm { flex-basis: 0px; flex-grow: 1; max-width: 100%; }
  .col-sm-auto { flex: 0 0 auto; width: auto; max-width: 100%; }
  .col-sm-1 { flex: 0 0 8.33333%; max-width: 8.33333%; }
  .col-sm-2 { flex: 0 0 16.6667%; max-width: 16.6667%; }
  .col-sm-3 { flex: 0 0 25%; max-width: 25%; }
  .col-sm-4 { flex: 0 0 33.3333%; max-width: 33.3333%; }
  .col-sm-5 { flex: 0 0 41.6667%; max-width: 41.6667%; }
  .col-sm-6 { flex: 0 0 50%; max-width: 50%; }
  .col-sm-7 { flex: 0 0 58.3333%; max-width: 58.3333%; }
  .col-sm-8 { flex: 0 0 66.6667%; max-width: 66.6667%; }
  .col-sm-9 { flex: 0 0 75%; max-width: 75%; }
  .col-sm-10 { flex: 0 0 83.3333%; max-width: 83.3333%; }
  .col-sm-11 { flex: 0 0 91.6667%; max-width: 91.6667%; }
  .col-sm-12 { flex: 0 0 100%; max-width: 100%; }
  .order-sm-first { order: -1; }
  .order-sm-last { order: 13; }
  .order-sm-0 { order: 0; }
  .order-sm-1 { order: 1; }
  .order-sm-2 { order: 2; }
  .order-sm-3 { order: 3; }
  .order-sm-4 { order: 4; }
  .order-sm-5 { order: 5; }
  .order-sm-6 { order: 6; }
  .order-sm-7 { order: 7; }
  .order-sm-8 { order: 8; }
  .order-sm-9 { order: 9; }
  .order-sm-10 { order: 10; }
  .order-sm-11 { order: 11; }
  .order-sm-12 { order: 12; }
  .offset-sm-0 { margin-left: 0px; }
  .offset-sm-1 { margin-left: 8.33333%; }
  .offset-sm-2 { margin-left: 16.6667%; }
  .offset-sm-3 { margin-left: 25%; }
  .offset-sm-4 { margin-left: 33.3333%; }
  .offset-sm-5 { margin-left: 41.6667%; }
  .offset-sm-6 { margin-left: 50%; }
  .offset-sm-7 { margin-left: 58.3333%; }
  .offset-sm-8 { margin-left: 66.6667%; }
  .offset-sm-9 { margin-left: 75%; }
  .offset-sm-10 { margin-left: 83.3333%; }
  .offset-sm-11 { margin-left: 91.6667%; }
}

@media (min-width: 768px) {
  .col-md { flex-basis: 0px; flex-grow: 1; max-width: 100%; }
  .col-md-auto { flex: 0 0 auto; width: auto; max-width: 100%; }
  .col-md-1 { flex: 0 0 8.33333%; max-width: 8.33333%; }
  .col-md-2 { flex: 0 0 16.6667%; max-width: 16.6667%; }
  .col-md-3 { flex: 0 0 25%; max-width: 25%; }
  .col-md-4 { flex: 0 0 33.3333%; max-width: 33.3333%; }
  .col-md-5 { flex: 0 0 41.6667%; max-width: 41.6667%; }
  .col-md-6 { flex: 0 0 50%; max-width: 50%; }
  .col-md-7 { flex: 0 0 58.3333%; max-width: 58.3333%; }
  .col-md-8 { flex: 0 0 66.6667%; max-width: 66.6667%; }
  .col-md-9 { flex: 0 0 75%; max-width: 75%; }
  .col-md-10 { flex: 0 0 83.3333%; max-width: 83.3333%; }
  .col-md-11 { flex: 0 0 91.6667%; max-width: 91.6667%; }
  .col-md-12 { flex: 0 0 100%; max-width: 100%; }
  .order-md-first { order: -1; }
  .order-md-last { order: 13; }
  .order-md-0 { order: 0; }
  .order-md-1 { order: 1; }
  .order-md-2 { order: 2; }
  .order-md-3 { order: 3; }
  .order-md-4 { order: 4; }
  .order-md-5 { order: 5; }
  .order-md-6 { order: 6; }
  .order-md-7 { order: 7; }
  .order-md-8 { order: 8; }
  .order-md-9 { order: 9; }
  .order-md-10 { order: 10; }
  .order-md-11 { order: 11; }
  .order-md-12 { order: 12; }
  .offset-md-0 { margin-left: 0px; }
  .offset-md-1 { margin-left: 8.33333%; }
  .offset-md-2 { margin-left: 16.6667%; }
  .offset-md-3 { margin-left: 25%; }
  .offset-md-4 { margin-left: 33.3333%; }
  .offset-md-5 { margin-left: 41.6667%; }
  .offset-md-6 { margin-left: 50%; }
  .offset-md-7 { margin-left: 58.3333%; }
  .offset-md-8 { margin-left: 66.6667%; }
  .offset-md-9 { margin-left: 75%; }
  .offset-md-10 { margin-left: 83.3333%; }
  .offset-md-11 { margin-left: 91.6667%; }
}

@media (min-width: 992px) {
  .col-lg { flex-basis: 0px; flex-grow: 1; max-width: 100%; }
  .col-lg-auto { flex: 0 0 auto; width: auto; max-width: 100%; }
  .col-lg-1 { flex: 0 0 8.33333%; max-width: 8.33333%; }
  .col-lg-2 { flex: 0 0 16.6667%; max-width: 16.6667%; }
  .col-lg-3 { flex: 0 0 25%; max-width: 25%; }
  .col-lg-4 { flex: 0 0 33.3333%; max-width: 33.3333%; }
  .col-lg-5 { flex: 0 0 41.6667%; max-width: 41.6667%; }
  .col-lg-6 { flex: 0 0 50%; max-width: 50%; }
  .col-lg-7 { flex: 0 0 58.3333%; max-width: 58.3333%; }
  .col-lg-8 { flex: 0 0 66.6667%; max-width: 66.6667%; }
  .col-lg-9 { flex: 0 0 75%; max-width: 75%; }
  .col-lg-10 { flex: 0 0 83.3333%; max-width: 83.3333%; }
  .col-lg-11 { flex: 0 0 91.6667%; max-width: 91.6667%; }
  .col-lg-12 { flex: 0 0 100%; max-width: 100%; }
  .order-lg-first { order: -1; }
  .order-lg-last { order: 13; }
  .order-lg-0 { order: 0; }
  .order-lg-1 { order: 1; }
  .order-lg-2 { order: 2; }
  .order-lg-3 { order: 3; }
  .order-lg-4 { order: 4; }
  .order-lg-5 { order: 5; }
  .order-lg-6 { order: 6; }
  .order-lg-7 { order: 7; }
  .order-lg-8 { order: 8; }
  .order-lg-9 { order: 9; }
  .order-lg-10 { order: 10; }
  .order-lg-11 { order: 11; }
  .order-lg-12 { order: 12; }
  .offset-lg-0 { margin-left: 0px; }
  .offset-lg-1 { margin-left: 8.33333%; }
  .offset-lg-2 { margin-left: 16.6667%; }
  .offset-lg-3 { margin-left: 25%; }
  .offset-lg-4 { margin-left: 33.3333%; }
  .offset-lg-5 { margin-left: 41.6667%; }
  .offset-lg-6 { margin-left: 50%; }
  .offset-lg-7 { margin-left: 58.3333%; }
  .offset-lg-8 { margin-left: 66.6667%; }
  .offset-lg-9 { margin-left: 75%; }
  .offset-lg-10 { margin-left: 83.3333%; }
  .offset-lg-11 { margin-left: 91.6667%; }
}

@media (min-width: 1200px) {
  .col-xl { flex-basis: 0px; flex-grow: 1; max-width: 100%; }
  .col-xl-auto { flex: 0 0 auto; width: auto; max-width: 100%; }
  .col-xl-1 { flex: 0 0 8.33333%; max-width: 8.33333%; }
  .col-xl-2 { flex: 0 0 16.6667%; max-width: 16.6667%; }
  .col-xl-3 { flex: 0 0 25%; max-width: 25%; }
  .col-xl-4 { flex: 0 0 33.3333%; max-width: 33.3333%; }
  .col-xl-5 { flex: 0 0 41.6667%; max-width: 41.6667%; }
  .col-xl-6 { flex: 0 0 50%; max-width: 50%; }
  .col-xl-7 { flex: 0 0 58.3333%; max-width: 58.3333%; }
  .col-xl-8 { flex: 0 0 66.6667%; max-width: 66.6667%; }
  .col-xl-9 { flex: 0 0 75%; max-width: 75%; }
  .col-xl-10 { flex: 0 0 83.3333%; max-width: 83.3333%; }
  .col-xl-11 { flex: 0 0 91.6667%; max-width: 91.6667%; }
  .col-xl-12 { flex: 0 0 100%; max-width: 100%; }
  .order-xl-first { order: -1; }
  .order-xl-last { order: 13; }
  .order-xl-0 { order: 0; }
  .order-xl-1 { order: 1; }
  .order-xl-2 { order: 2; }
  .order-xl-3 { order: 3; }
  .order-xl-4 { order: 4; }
  .order-xl-5 { order: 5; }
  .order-xl-6 { order: 6; }
  .order-xl-7 { order: 7; }
  .order-xl-8 { order: 8; }
  .order-xl-9 { order: 9; }
  .order-xl-10 { order: 10; }
  .order-xl-11 { order: 11; }
  .order-xl-12 { order: 12; }
  .offset-xl-0 { margin-left: 0px; }
  .offset-xl-1 { margin-left: 8.33333%; }
  .offset-xl-2 { margin-left: 16.6667%; }
  .offset-xl-3 { margin-left: 25%; }
  .offset-xl-4 { margin-left: 33.3333%; }
  .offset-xl-5 { margin-left: 41.6667%; }
  .offset-xl-6 { margin-left: 50%; }
  .offset-xl-7 { margin-left: 58.3333%; }
  .offset-xl-8 { margin-left: 66.6667%; }
  .offset-xl-9 { margin-left: 75%; }
  .offset-xl-10 { margin-left: 83.3333%; }
  .offset-xl-11 { margin-left: 91.6667%; }
}

.table { width: 100%; margin-bottom: 1rem; color: rgb(33, 37, 41); }

.table td, .table th { padding: 0.75rem; vertical-align: top; border-top: 1=
px solid rgb(222, 226, 230); }

.table thead th { vertical-align: bottom; border-bottom: 2px solid rgb(222,=
 226, 230); }

.table tbody + tbody { border-top: 2px solid rgb(222, 226, 230); }

.table-sm td, .table-sm th { padding: 0.3rem; }

.table-bordered { border: 1px solid rgb(222, 226, 230); }

.table-bordered td, .table-bordered th { border: 1px solid rgb(222, 226, 23=
0); }

.table-bordered thead td, .table-bordered thead th { border-bottom-width: 2=
px; }

.table-borderless tbody + tbody, .table-borderless td, .table-borderless th=
, .table-borderless thead th { border: 0px; }

.table-striped tbody tr:nth-of-type(2n+1) { background-color: rgba(0, 0, 0,=
 0.05); }

.table-hover tbody tr:hover { color: rgb(33, 37, 41); background-color: rgb=
a(0, 0, 0, 0.075); }

.table-primary, .table-primary > td, .table-primary > th { background-color=
: rgb(184, 218, 255); }

.table-primary tbody + tbody, .table-primary td, .table-primary th, .table-=
primary thead th { border-color: rgb(122, 186, 255); }

.table-hover .table-primary:hover { background-color: rgb(159, 205, 255); }

.table-hover .table-primary:hover > td, .table-hover .table-primary:hover >=
 th { background-color: rgb(159, 205, 255); }

.table-secondary, .table-secondary > td, .table-secondary > th { background=
-color: rgb(214, 216, 219); }

.table-secondary tbody + tbody, .table-secondary td, .table-secondary th, .=
table-secondary thead th { border-color: rgb(179, 183, 187); }

.table-hover .table-secondary:hover { background-color: rgb(200, 203, 207);=
 }

.table-hover .table-secondary:hover > td, .table-hover .table-secondary:hov=
er > th { background-color: rgb(200, 203, 207); }

.table-success, .table-success > td, .table-success > th { background-color=
: rgb(195, 230, 203); }

.table-success tbody + tbody, .table-success td, .table-success th, .table-=
success thead th { border-color: rgb(143, 209, 158); }

.table-hover .table-success:hover { background-color: rgb(177, 223, 187); }

.table-hover .table-success:hover > td, .table-hover .table-success:hover >=
 th { background-color: rgb(177, 223, 187); }

.table-info, .table-info > td, .table-info > th { background-color: rgb(190=
, 229, 235); }

.table-info tbody + tbody, .table-info td, .table-info th, .table-info thea=
d th { border-color: rgb(134, 207, 218); }

.table-hover .table-info:hover { background-color: rgb(171, 221, 229); }

.table-hover .table-info:hover > td, .table-hover .table-info:hover > th { =
background-color: rgb(171, 221, 229); }

.table-warning, .table-warning > td, .table-warning > th { background-color=
: rgb(255, 238, 186); }

.table-warning tbody + tbody, .table-warning td, .table-warning th, .table-=
warning thead th { border-color: rgb(255, 223, 126); }

.table-hover .table-warning:hover { background-color: rgb(255, 232, 161); }

.table-hover .table-warning:hover > td, .table-hover .table-warning:hover >=
 th { background-color: rgb(255, 232, 161); }

.table-danger, .table-danger > td, .table-danger > th { background-color: r=
gb(245, 198, 203); }

.table-danger tbody + tbody, .table-danger td, .table-danger th, .table-dan=
ger thead th { border-color: rgb(237, 150, 158); }

.table-hover .table-danger:hover { background-color: rgb(241, 176, 183); }

.table-hover .table-danger:hover > td, .table-hover .table-danger:hover > t=
h { background-color: rgb(241, 176, 183); }

.table-light, .table-light > td, .table-light > th { background-color: rgb(=
253, 253, 254); }

.table-light tbody + tbody, .table-light td, .table-light th, .table-light =
thead th { border-color: rgb(251, 252, 252); }

.table-hover .table-light:hover { background-color: rgb(236, 236, 246); }

.table-hover .table-light:hover > td, .table-hover .table-light:hover > th =
{ background-color: rgb(236, 236, 246); }

.table-dark, .table-dark > td, .table-dark > th { background-color: rgb(198=
, 200, 202); }

.table-dark tbody + tbody, .table-dark td, .table-dark th, .table-dark thea=
d th { border-color: rgb(149, 153, 156); }

.table-hover .table-dark:hover { background-color: rgb(185, 187, 190); }

.table-hover .table-dark:hover > td, .table-hover .table-dark:hover > th { =
background-color: rgb(185, 187, 190); }

.table-active, .table-active > td, .table-active > th { background-color: r=
gba(0, 0, 0, 0.075); }

.table-hover .table-active:hover { background-color: rgba(0, 0, 0, 0.075); =
}

.table-hover .table-active:hover > td, .table-hover .table-active:hover > t=
h { background-color: rgba(0, 0, 0, 0.075); }

.table .thead-dark th { color: rgb(255, 255, 255); background-color: rgb(52=
, 58, 64); border-color: rgb(69, 77, 85); }

.table .thead-light th { color: rgb(73, 80, 87); background-color: rgb(233,=
 236, 239); border-color: rgb(222, 226, 230); }

.table-dark { color: rgb(255, 255, 255); background-color: rgb(52, 58, 64);=
 }

.table-dark td, .table-dark th, .table-dark thead th { border-color: rgb(69=
, 77, 85); }

.table-dark.table-bordered { border: 0px; }

.table-dark.table-striped tbody tr:nth-of-type(2n+1) { background-color: rg=
ba(255, 255, 255, 0.05); }

.table-dark.table-hover tbody tr:hover { color: rgb(255, 255, 255); backgro=
und-color: rgba(255, 255, 255, 0.075); }

@media (max-width: 575.98px) {
  .table-responsive-sm { display: block; width: 100%; overflow-x: auto; }
  .table-responsive-sm > .table-bordered { border: 0px; }
}

@media (max-width: 767.98px) {
  .table-responsive-md { display: block; width: 100%; overflow-x: auto; }
  .table-responsive-md > .table-bordered { border: 0px; }
}

@media (max-width: 991.98px) {
  .table-responsive-lg { display: block; width: 100%; overflow-x: auto; }
  .table-responsive-lg > .table-bordered { border: 0px; }
}

@media (max-width: 1199.98px) {
  .table-responsive-xl { display: block; width: 100%; overflow-x: auto; }
  .table-responsive-xl > .table-bordered { border: 0px; }
}

.table-responsive { display: block; width: 100%; overflow-x: auto; }

.table-responsive > .table-bordered { border: 0px; }

.form-control { display: block; width: 100%; height: calc(1.5em + 0.75rem +=
 2px); padding: 0.375rem 0.75rem; font-size: 1rem; font-weight: 400; line-h=
eight: 1.5; color: rgb(73, 80, 87); background-color: rgb(255, 255, 255); b=
ackground-clip: padding-box; border: 1px solid rgb(206, 212, 218); border-r=
adius: 0.25rem; transition: border-color 0.15s ease-in-out 0s, box-shadow 0=
.15s ease-in-out 0s; }

@media (prefers-reduced-motion: reduce) {
  .form-control { transition: none 0s ease 0s; }
}

.form-control:focus { color: rgb(73, 80, 87); background-color: rgb(255, 25=
5, 255); border-color: rgb(128, 189, 255); outline: 0px; box-shadow: rgba(0=
, 123, 255, 0.25) 0px 0px 0px 0.2rem; }

.form-control::-webkit-input-placeholder { color: rgb(108, 117, 125); opaci=
ty: 1; }

.form-control::placeholder { color: rgb(108, 117, 125); opacity: 1; }

.form-control:disabled, .form-control[readonly] { background-color: rgb(233=
, 236, 239); opacity: 1; }

.form-control-file, .form-control-range { display: block; width: 100%; }

.col-form-label { padding-top: calc(0.375rem + 1px); padding-bottom: calc(0=
.375rem + 1px); margin-bottom: 0px; font-size: inherit; line-height: 1.5; }

.col-form-label-lg { padding-top: calc(0.5rem + 1px); padding-bottom: calc(=
0.5rem + 1px); font-size: 1.25rem; line-height: 1.5; }

.col-form-label-sm { padding-top: calc(0.25rem + 1px); padding-bottom: calc=
(0.25rem + 1px); font-size: 0.875rem; line-height: 1.5; }

.form-control-plaintext { display: block; width: 100%; padding-top: 0.375re=
m; padding-bottom: 0.375rem; margin-bottom: 0px; line-height: 1.5; color: r=
gb(33, 37, 41); background-color: transparent; border-style: solid; border-=
color: transparent; border-image: initial; border-width: 1px 0px; }

.form-control-plaintext.form-control-lg, .form-control-plaintext.form-contr=
ol-sm { padding-right: 0px; padding-left: 0px; }

.form-control-sm { height: calc(1.5em + 0.5rem + 2px); padding: 0.25rem 0.5=
rem; font-size: 0.875rem; line-height: 1.5; border-radius: 0.2rem; }

.form-control-lg { height: calc(1.5em + 1rem + 2px); padding: 0.5rem 1rem; =
font-size: 1.25rem; line-height: 1.5; border-radius: 0.3rem; }

select.form-control[multiple], select.form-control[size] { height: auto; }

textarea.form-control { height: auto; }

.form-group { margin-bottom: 1rem; }

.form-text { display: block; margin-top: 0.25rem; }

.form-row { display: flex; flex-wrap: wrap; margin-right: -5px; margin-left=
: -5px; }

.form-row > .col, .form-row > [class*=3D"col-"] { padding-right: 5px; paddi=
ng-left: 5px; }

.form-check { position: relative; display: block; padding-left: 1.25rem; }

.form-check-input { position: absolute; margin-top: 0.3rem; margin-left: -1=
.25rem; }

.form-check-input:disabled ~ .form-check-label { color: rgb(108, 117, 125);=
 }

.form-check-label { margin-bottom: 0px; }

.form-check-inline { display: inline-flex; align-items: center; padding-lef=
t: 0px; margin-right: 0.75rem; }

.form-check-inline .form-check-input { position: static; margin-top: 0px; m=
argin-right: 0.3125rem; margin-left: 0px; }

.valid-feedback { display: none; width: 100%; margin-top: 0.25rem; font-siz=
e: 80%; color: rgb(40, 167, 69); }

.valid-tooltip { position: absolute; top: 100%; z-index: 5; display: none; =
max-width: 100%; padding: 0.25rem 0.5rem; margin-top: 0.1rem; font-size: 0.=
875rem; line-height: 1.5; color: rgb(255, 255, 255); background-color: rgba=
(40, 167, 69, 0.9); border-radius: 0.25rem; }

.form-control.is-valid, .was-validated .form-control:valid { border-color: =
rgb(40, 167, 69); padding-right: calc(1.5em + 0.75rem); background-image: u=
rl("data:image/svg+xml,%3csvg xmlns=3D'http://www.w3.org/2000/svg' viewBox=
=3D'0 0 8 8'%3e%3cpath fill=3D'%2328a745' d=3D'M2.3 6.73L.6 4.53c-.4-1.04.4=
6-1.4 1.1-.8l1.1 1.4 3.4-3.8c.6-.63 1.6-.27 1.2.7l-4 4.6c-.43.5-.8.4-1.1.1z=
'/%3e%3c/svg%3e"); background-repeat: no-repeat; background-position: right=
 calc(0.375em + 0.1875rem) center; background-size: calc(0.75em + 0.375rem)=
 calc(0.75em + 0.375rem); }

.form-control.is-valid:focus, .was-validated .form-control:valid:focus { bo=
rder-color: rgb(40, 167, 69); box-shadow: rgba(40, 167, 69, 0.25) 0px 0px 0=
px 0.2rem; }

.form-control.is-valid ~ .valid-feedback, .form-control.is-valid ~ .valid-t=
ooltip, .was-validated .form-control:valid ~ .valid-feedback, .was-validate=
d .form-control:valid ~ .valid-tooltip { display: block; }

.was-validated textarea.form-control:valid, textarea.form-control.is-valid =
{ padding-right: calc(1.5em + 0.75rem); background-position: right calc(0.3=
75em + 0.1875rem) top calc(0.375em + 0.1875rem); }

.custom-select.is-valid, .was-validated .custom-select:valid { border-color=
: rgb(40, 167, 69); padding-right: calc(((1em + 0.75rem) * 3) / 4 + 1.75rem=
); background: url("data:image/svg+xml,%3csvg xmlns=3D'http://www.w3.org/20=
00/svg' viewBox=3D'0 0 4 5'%3e%3cpath fill=3D'%23343a40' d=3D'M2 0L0 2h4zm0=
 5L0 3h4z'/%3e%3c/svg%3e") right 0.75rem center / 8px 10px no-repeat, url("=
data:image/svg+xml,%3csvg xmlns=3D'http://www.w3.org/2000/svg' viewBox=3D'0=
 0 8 8'%3e%3cpath fill=3D'%2328a745' d=3D'M2.3 6.73L.6 4.53c-.4-1.04.46-1.4=
 1.1-.8l1.1 1.4 3.4-3.8c.6-.63 1.6-.27 1.2.7l-4 4.6c-.43.5-.8.4-1.1.1z'/%3e=
%3c/svg%3e") right 1.75rem center / calc(0.75em + 0.375rem) calc(0.75em + 0=
.375rem) no-repeat rgb(255, 255, 255); }

.custom-select.is-valid:focus, .was-validated .custom-select:valid:focus { =
border-color: rgb(40, 167, 69); box-shadow: rgba(40, 167, 69, 0.25) 0px 0px=
 0px 0.2rem; }

.custom-select.is-valid ~ .valid-feedback, .custom-select.is-valid ~ .valid=
-tooltip, .was-validated .custom-select:valid ~ .valid-feedback, .was-valid=
ated .custom-select:valid ~ .valid-tooltip { display: block; }

.form-control-file.is-valid ~ .valid-feedback, .form-control-file.is-valid =
~ .valid-tooltip, .was-validated .form-control-file:valid ~ .valid-feedback=
, .was-validated .form-control-file:valid ~ .valid-tooltip { display: block=
; }

.form-check-input.is-valid ~ .form-check-label, .was-validated .form-check-=
input:valid ~ .form-check-label { color: rgb(40, 167, 69); }

.form-check-input.is-valid ~ .valid-feedback, .form-check-input.is-valid ~ =
.valid-tooltip, .was-validated .form-check-input:valid ~ .valid-feedback, .=
was-validated .form-check-input:valid ~ .valid-tooltip { display: block; }

.custom-control-input.is-valid ~ .custom-control-label, .was-validated .cus=
tom-control-input:valid ~ .custom-control-label { color: rgb(40, 167, 69); =
}

.custom-control-input.is-valid ~ .custom-control-label::before, .was-valida=
ted .custom-control-input:valid ~ .custom-control-label::before { border-co=
lor: rgb(40, 167, 69); }

.custom-control-input.is-valid ~ .valid-feedback, .custom-control-input.is-=
valid ~ .valid-tooltip, .was-validated .custom-control-input:valid ~ .valid=
-feedback, .was-validated .custom-control-input:valid ~ .valid-tooltip { di=
splay: block; }

.custom-control-input.is-valid:checked ~ .custom-control-label::before, .wa=
s-validated .custom-control-input:valid:checked ~ .custom-control-label::be=
fore { border-color: rgb(52, 206, 87); background-color: rgb(52, 206, 87); =
}

.custom-control-input.is-valid:focus ~ .custom-control-label::before, .was-=
validated .custom-control-input:valid:focus ~ .custom-control-label::before=
 { box-shadow: rgba(40, 167, 69, 0.25) 0px 0px 0px 0.2rem; }

.custom-control-input.is-valid:focus:not(:checked) ~ .custom-control-label:=
:before, .was-validated .custom-control-input:valid:focus:not(:checked) ~ .=
custom-control-label::before { border-color: rgb(40, 167, 69); }

.custom-file-input.is-valid ~ .custom-file-label, .was-validated .custom-fi=
le-input:valid ~ .custom-file-label { border-color: rgb(40, 167, 69); }

.custom-file-input.is-valid ~ .valid-feedback, .custom-file-input.is-valid =
~ .valid-tooltip, .was-validated .custom-file-input:valid ~ .valid-feedback=
, .was-validated .custom-file-input:valid ~ .valid-tooltip { display: block=
; }

.custom-file-input.is-valid:focus ~ .custom-file-label, .was-validated .cus=
tom-file-input:valid:focus ~ .custom-file-label { border-color: rgb(40, 167=
, 69); box-shadow: rgba(40, 167, 69, 0.25) 0px 0px 0px 0.2rem; }

.invalid-feedback { display: none; width: 100%; margin-top: 0.25rem; font-s=
ize: 80%; color: rgb(220, 53, 69); }

.invalid-tooltip { position: absolute; top: 100%; z-index: 5; display: none=
; max-width: 100%; padding: 0.25rem 0.5rem; margin-top: 0.1rem; font-size: =
0.875rem; line-height: 1.5; color: rgb(255, 255, 255); background-color: rg=
ba(220, 53, 69, 0.9); border-radius: 0.25rem; }

.form-control.is-invalid, .was-validated .form-control:invalid { border-col=
or: rgb(220, 53, 69); padding-right: calc(1.5em + 0.75rem); background-imag=
e: url("data:image/svg+xml,%3csvg xmlns=3D'http://www.w3.org/2000/svg' fill=
=3D'%23dc3545' viewBox=3D'-2 -2 7 7'%3e%3cpath stroke=3D'%23dc3545' d=3D'M0=
 0l3 3m0-3L0 3'/%3e%3ccircle r=3D'.5'/%3e%3ccircle cx=3D'3' r=3D'.5'/%3e%3c=
circle cy=3D'3' r=3D'.5'/%3e%3ccircle cx=3D'3' cy=3D'3' r=3D'.5'/%3e%3c/svg=
%3E"); background-repeat: no-repeat; background-position: right calc(0.375e=
m + 0.1875rem) center; background-size: calc(0.75em + 0.375rem) calc(0.75em=
 + 0.375rem); }

.form-control.is-invalid:focus, .was-validated .form-control:invalid:focus =
{ border-color: rgb(220, 53, 69); box-shadow: rgba(220, 53, 69, 0.25) 0px 0=
px 0px 0.2rem; }

.form-control.is-invalid ~ .invalid-feedback, .form-control.is-invalid ~ .i=
nvalid-tooltip, .was-validated .form-control:invalid ~ .invalid-feedback, .=
was-validated .form-control:invalid ~ .invalid-tooltip { display: block; }

.was-validated textarea.form-control:invalid, textarea.form-control.is-inva=
lid { padding-right: calc(1.5em + 0.75rem); background-position: right calc=
(0.375em + 0.1875rem) top calc(0.375em + 0.1875rem); }

.custom-select.is-invalid, .was-validated .custom-select:invalid { border-c=
olor: rgb(220, 53, 69); padding-right: calc(((1em + 0.75rem) * 3) / 4 + 1.7=
5rem); background: url("data:image/svg+xml,%3csvg xmlns=3D'http://www.w3.or=
g/2000/svg' viewBox=3D'0 0 4 5'%3e%3cpath fill=3D'%23343a40' d=3D'M2 0L0 2h=
4zm0 5L0 3h4z'/%3e%3c/svg%3e") right 0.75rem center / 8px 10px no-repeat, u=
rl("data:image/svg+xml,%3csvg xmlns=3D'http://www.w3.org/2000/svg' fill=3D'=
%23dc3545' viewBox=3D'-2 -2 7 7'%3e%3cpath stroke=3D'%23dc3545' d=3D'M0 0l3=
 3m0-3L0 3'/%3e%3ccircle r=3D'.5'/%3e%3ccircle cx=3D'3' r=3D'.5'/%3e%3ccirc=
le cy=3D'3' r=3D'.5'/%3e%3ccircle cx=3D'3' cy=3D'3' r=3D'.5'/%3e%3c/svg%3E"=
) right 1.75rem center / calc(0.75em + 0.375rem) calc(0.75em + 0.375rem) no=
-repeat rgb(255, 255, 255); }

.custom-select.is-invalid:focus, .was-validated .custom-select:invalid:focu=
s { border-color: rgb(220, 53, 69); box-shadow: rgba(220, 53, 69, 0.25) 0px=
 0px 0px 0.2rem; }

.custom-select.is-invalid ~ .invalid-feedback, .custom-select.is-invalid ~ =
.invalid-tooltip, .was-validated .custom-select:invalid ~ .invalid-feedback=
, .was-validated .custom-select:invalid ~ .invalid-tooltip { display: block=
; }

.form-control-file.is-invalid ~ .invalid-feedback, .form-control-file.is-in=
valid ~ .invalid-tooltip, .was-validated .form-control-file:invalid ~ .inva=
lid-feedback, .was-validated .form-control-file:invalid ~ .invalid-tooltip =
{ display: block; }

.form-check-input.is-invalid ~ .form-check-label, .was-validated .form-chec=
k-input:invalid ~ .form-check-label { color: rgb(220, 53, 69); }

.form-check-input.is-invalid ~ .invalid-feedback, .form-check-input.is-inva=
lid ~ .invalid-tooltip, .was-validated .form-check-input:invalid ~ .invalid=
-feedback, .was-validated .form-check-input:invalid ~ .invalid-tooltip { di=
splay: block; }

.custom-control-input.is-invalid ~ .custom-control-label, .was-validated .c=
ustom-control-input:invalid ~ .custom-control-label { color: rgb(220, 53, 6=
9); }

.custom-control-input.is-invalid ~ .custom-control-label::before, .was-vali=
dated .custom-control-input:invalid ~ .custom-control-label::before { borde=
r-color: rgb(220, 53, 69); }

.custom-control-input.is-invalid ~ .invalid-feedback, .custom-control-input=
.is-invalid ~ .invalid-tooltip, .was-validated .custom-control-input:invali=
d ~ .invalid-feedback, .was-validated .custom-control-input:invalid ~ .inva=
lid-tooltip { display: block; }

.custom-control-input.is-invalid:checked ~ .custom-control-label::before, .=
was-validated .custom-control-input:invalid:checked ~ .custom-control-label=
::before { border-color: rgb(228, 96, 109); background-color: rgb(228, 96, =
109); }

.custom-control-input.is-invalid:focus ~ .custom-control-label::before, .wa=
s-validated .custom-control-input:invalid:focus ~ .custom-control-label::be=
fore { box-shadow: rgba(220, 53, 69, 0.25) 0px 0px 0px 0.2rem; }

.custom-control-input.is-invalid:focus:not(:checked) ~ .custom-control-labe=
l::before, .was-validated .custom-control-input:invalid:focus:not(:checked)=
 ~ .custom-control-label::before { border-color: rgb(220, 53, 69); }

.custom-file-input.is-invalid ~ .custom-file-label, .was-validated .custom-=
file-input:invalid ~ .custom-file-label { border-color: rgb(220, 53, 69); }

.custom-file-input.is-invalid ~ .invalid-feedback, .custom-file-input.is-in=
valid ~ .invalid-tooltip, .was-validated .custom-file-input:invalid ~ .inva=
lid-feedback, .was-validated .custom-file-input:invalid ~ .invalid-tooltip =
{ display: block; }

.custom-file-input.is-invalid:focus ~ .custom-file-label, .was-validated .c=
ustom-file-input:invalid:focus ~ .custom-file-label { border-color: rgb(220=
, 53, 69); box-shadow: rgba(220, 53, 69, 0.25) 0px 0px 0px 0.2rem; }

.form-inline { display: flex; flex-flow: row wrap; align-items: center; }

.form-inline .form-check { width: 100%; }

@media (min-width: 576px) {
  .form-inline label { display: flex; align-items: center; justify-content:=
 center; margin-bottom: 0px; }
  .form-inline .form-group { display: flex; flex: 0 0 auto; flex-flow: row =
wrap; align-items: center; margin-bottom: 0px; }
  .form-inline .form-control { display: inline-block; width: auto; vertical=
-align: middle; }
  .form-inline .form-control-plaintext { display: inline-block; }
  .form-inline .custom-select, .form-inline .input-group { width: auto; }
  .form-inline .form-check { display: flex; align-items: center; justify-co=
ntent: center; width: auto; padding-left: 0px; }
  .form-inline .form-check-input { position: relative; flex-shrink: 0; marg=
in-top: 0px; margin-right: 0.25rem; margin-left: 0px; }
  .form-inline .custom-control { align-items: center; justify-content: cent=
er; }
  .form-inline .custom-control-label { margin-bottom: 0px; }
}

.btn { display: inline-block; font-weight: 400; color: rgb(33, 37, 41); tex=
t-align: center; vertical-align: middle; user-select: none; background-colo=
r: transparent; border: 1px solid transparent; padding: 0.375rem 0.75rem; f=
ont-size: 1rem; line-height: 1.5; border-radius: 0.25rem; transition: color=
 0.15s ease-in-out 0s, background-color 0.15s ease-in-out 0s, border-color =
0.15s ease-in-out 0s, box-shadow 0.15s ease-in-out 0s; }

@media (prefers-reduced-motion: reduce) {
  .btn { transition: none 0s ease 0s; }
}

.btn:hover { color: rgb(33, 37, 41); text-decoration: none; }

.btn.focus, .btn:focus { outline: 0px; box-shadow: rgba(0, 123, 255, 0.25) =
0px 0px 0px 0.2rem; }

.btn.disabled, .btn:disabled { opacity: 0.65; }

a.btn.disabled, fieldset:disabled a.btn { pointer-events: none; }

.btn-primary { color: rgb(255, 255, 255); background-color: rgb(0, 123, 255=
); border-color: rgb(0, 123, 255); }

.btn-primary:hover { color: rgb(255, 255, 255); background-color: rgb(0, 10=
5, 217); border-color: rgb(0, 98, 204); }

.btn-primary.focus, .btn-primary:focus { box-shadow: rgba(38, 143, 255, 0.5=
) 0px 0px 0px 0.2rem; }

.btn-primary.disabled, .btn-primary:disabled { color: rgb(255, 255, 255); b=
ackground-color: rgb(0, 123, 255); border-color: rgb(0, 123, 255); }

.btn-primary:not(:disabled):not(.disabled).active, .btn-primary:not(:disabl=
ed):not(.disabled):active, .show > .btn-primary.dropdown-toggle { color: rg=
b(255, 255, 255); background-color: rgb(0, 98, 204); border-color: rgb(0, 9=
2, 191); }

.btn-primary:not(:disabled):not(.disabled).active:focus, .btn-primary:not(:=
disabled):not(.disabled):active:focus, .show > .btn-primary.dropdown-toggle=
:focus { box-shadow: rgba(38, 143, 255, 0.5) 0px 0px 0px 0.2rem; }

.btn-secondary { color: rgb(255, 255, 255); background-color: rgb(108, 117,=
 125); border-color: rgb(108, 117, 125); }

.btn-secondary:hover { color: rgb(255, 255, 255); background-color: rgb(90,=
 98, 104); border-color: rgb(84, 91, 98); }

.btn-secondary.focus, .btn-secondary:focus { box-shadow: rgba(130, 138, 145=
, 0.5) 0px 0px 0px 0.2rem; }

.btn-secondary.disabled, .btn-secondary:disabled { color: rgb(255, 255, 255=
); background-color: rgb(108, 117, 125); border-color: rgb(108, 117, 125); =
}

.btn-secondary:not(:disabled):not(.disabled).active, .btn-secondary:not(:di=
sabled):not(.disabled):active, .show > .btn-secondary.dropdown-toggle { col=
or: rgb(255, 255, 255); background-color: rgb(84, 91, 98); border-color: rg=
b(78, 85, 91); }

.btn-secondary:not(:disabled):not(.disabled).active:focus, .btn-secondary:n=
ot(:disabled):not(.disabled):active:focus, .show > .btn-secondary.dropdown-=
toggle:focus { box-shadow: rgba(130, 138, 145, 0.5) 0px 0px 0px 0.2rem; }

.btn-success { color: rgb(255, 255, 255); background-color: rgb(40, 167, 69=
); border-color: rgb(40, 167, 69); }

.btn-success:hover { color: rgb(255, 255, 255); background-color: rgb(33, 1=
36, 56); border-color: rgb(30, 126, 52); }

.btn-success.focus, .btn-success:focus { box-shadow: rgba(72, 180, 97, 0.5)=
 0px 0px 0px 0.2rem; }

.btn-success.disabled, .btn-success:disabled { color: rgb(255, 255, 255); b=
ackground-color: rgb(40, 167, 69); border-color: rgb(40, 167, 69); }

.btn-success:not(:disabled):not(.disabled).active, .btn-success:not(:disabl=
ed):not(.disabled):active, .show > .btn-success.dropdown-toggle { color: rg=
b(255, 255, 255); background-color: rgb(30, 126, 52); border-color: rgb(28,=
 116, 48); }

.btn-success:not(:disabled):not(.disabled).active:focus, .btn-success:not(:=
disabled):not(.disabled):active:focus, .show > .btn-success.dropdown-toggle=
:focus { box-shadow: rgba(72, 180, 97, 0.5) 0px 0px 0px 0.2rem; }

.btn-info { color: rgb(255, 255, 255); background-color: rgb(23, 162, 184);=
 border-color: rgb(23, 162, 184); }

.btn-info:hover { color: rgb(255, 255, 255); background-color: rgb(19, 132,=
 150); border-color: rgb(17, 122, 139); }

.btn-info.focus, .btn-info:focus { box-shadow: rgba(58, 176, 195, 0.5) 0px =
0px 0px 0.2rem; }

.btn-info.disabled, .btn-info:disabled { color: rgb(255, 255, 255); backgro=
und-color: rgb(23, 162, 184); border-color: rgb(23, 162, 184); }

.btn-info:not(:disabled):not(.disabled).active, .btn-info:not(:disabled):no=
t(.disabled):active, .show > .btn-info.dropdown-toggle { color: rgb(255, 25=
5, 255); background-color: rgb(17, 122, 139); border-color: rgb(16, 112, 12=
7); }

.btn-info:not(:disabled):not(.disabled).active:focus, .btn-info:not(:disabl=
ed):not(.disabled):active:focus, .show > .btn-info.dropdown-toggle:focus { =
box-shadow: rgba(58, 176, 195, 0.5) 0px 0px 0px 0.2rem; }

.btn-warning { color: rgb(33, 37, 41); background-color: rgb(255, 193, 7); =
border-color: rgb(255, 193, 7); }

.btn-warning:hover { color: rgb(33, 37, 41); background-color: rgb(224, 168=
, 0); border-color: rgb(211, 158, 0); }

.btn-warning.focus, .btn-warning:focus { box-shadow: rgba(222, 170, 12, 0.5=
) 0px 0px 0px 0.2rem; }

.btn-warning.disabled, .btn-warning:disabled { color: rgb(33, 37, 41); back=
ground-color: rgb(255, 193, 7); border-color: rgb(255, 193, 7); }

.btn-warning:not(:disabled):not(.disabled).active, .btn-warning:not(:disabl=
ed):not(.disabled):active, .show > .btn-warning.dropdown-toggle { color: rg=
b(33, 37, 41); background-color: rgb(211, 158, 0); border-color: rgb(198, 1=
49, 0); }

.btn-warning:not(:disabled):not(.disabled).active:focus, .btn-warning:not(:=
disabled):not(.disabled):active:focus, .show > .btn-warning.dropdown-toggle=
:focus { box-shadow: rgba(222, 170, 12, 0.5) 0px 0px 0px 0.2rem; }

.btn-danger { color: rgb(255, 255, 255); background-color: rgb(220, 53, 69)=
; border-color: rgb(220, 53, 69); }

.btn-danger:hover { color: rgb(255, 255, 255); background-color: rgb(200, 3=
5, 51); border-color: rgb(189, 33, 48); }

.btn-danger.focus, .btn-danger:focus { box-shadow: rgba(225, 83, 97, 0.5) 0=
px 0px 0px 0.2rem; }

.btn-danger.disabled, .btn-danger:disabled { color: rgb(255, 255, 255); bac=
kground-color: rgb(220, 53, 69); border-color: rgb(220, 53, 69); }

.btn-danger:not(:disabled):not(.disabled).active, .btn-danger:not(:disabled=
):not(.disabled):active, .show > .btn-danger.dropdown-toggle { color: rgb(2=
55, 255, 255); background-color: rgb(189, 33, 48); border-color: rgb(178, 3=
1, 45); }

.btn-danger:not(:disabled):not(.disabled).active:focus, .btn-danger:not(:di=
sabled):not(.disabled):active:focus, .show > .btn-danger.dropdown-toggle:fo=
cus { box-shadow: rgba(225, 83, 97, 0.5) 0px 0px 0px 0.2rem; }

.btn-light { color: rgb(33, 37, 41); background-color: rgb(248, 249, 250); =
border-color: rgb(248, 249, 250); }

.btn-light:hover { color: rgb(33, 37, 41); background-color: rgb(226, 230, =
234); border-color: rgb(218, 224, 229); }

.btn-light.focus, .btn-light:focus { box-shadow: rgba(216, 217, 219, 0.5) 0=
px 0px 0px 0.2rem; }

.btn-light.disabled, .btn-light:disabled { color: rgb(33, 37, 41); backgrou=
nd-color: rgb(248, 249, 250); border-color: rgb(248, 249, 250); }

.btn-light:not(:disabled):not(.disabled).active, .btn-light:not(:disabled):=
not(.disabled):active, .show > .btn-light.dropdown-toggle { color: rgb(33, =
37, 41); background-color: rgb(218, 224, 229); border-color: rgb(211, 217, =
223); }

.btn-light:not(:disabled):not(.disabled).active:focus, .btn-light:not(:disa=
bled):not(.disabled):active:focus, .show > .btn-light.dropdown-toggle:focus=
 { box-shadow: rgba(216, 217, 219, 0.5) 0px 0px 0px 0.2rem; }

.btn-dark { color: rgb(255, 255, 255); background-color: rgb(52, 58, 64); b=
order-color: rgb(52, 58, 64); }

.btn-dark:hover { color: rgb(255, 255, 255); background-color: rgb(35, 39, =
43); border-color: rgb(29, 33, 36); }

.btn-dark.focus, .btn-dark:focus { box-shadow: rgba(82, 88, 93, 0.5) 0px 0p=
x 0px 0.2rem; }

.btn-dark.disabled, .btn-dark:disabled { color: rgb(255, 255, 255); backgro=
und-color: rgb(52, 58, 64); border-color: rgb(52, 58, 64); }

.btn-dark:not(:disabled):not(.disabled).active, .btn-dark:not(:disabled):no=
t(.disabled):active, .show > .btn-dark.dropdown-toggle { color: rgb(255, 25=
5, 255); background-color: rgb(29, 33, 36); border-color: rgb(23, 26, 29); =
}

.btn-dark:not(:disabled):not(.disabled).active:focus, .btn-dark:not(:disabl=
ed):not(.disabled):active:focus, .show > .btn-dark.dropdown-toggle:focus { =
box-shadow: rgba(82, 88, 93, 0.5) 0px 0px 0px 0.2rem; }

.btn-outline-primary { color: rgb(0, 123, 255); border-color: rgb(0, 123, 2=
55); }

.btn-outline-primary:hover { color: rgb(255, 255, 255); background-color: r=
gb(0, 123, 255); border-color: rgb(0, 123, 255); }

.btn-outline-primary.focus, .btn-outline-primary:focus { box-shadow: rgba(0=
, 123, 255, 0.5) 0px 0px 0px 0.2rem; }

.btn-outline-primary.disabled, .btn-outline-primary:disabled { color: rgb(0=
, 123, 255); background-color: transparent; }

.btn-outline-primary:not(:disabled):not(.disabled).active, .btn-outline-pri=
mary:not(:disabled):not(.disabled):active, .show > .btn-outline-primary.dro=
pdown-toggle { color: rgb(255, 255, 255); background-color: rgb(0, 123, 255=
); border-color: rgb(0, 123, 255); }

.btn-outline-primary:not(:disabled):not(.disabled).active:focus, .btn-outli=
ne-primary:not(:disabled):not(.disabled):active:focus, .show > .btn-outline=
-primary.dropdown-toggle:focus { box-shadow: rgba(0, 123, 255, 0.5) 0px 0px=
 0px 0.2rem; }

.btn-outline-secondary { color: rgb(108, 117, 125); border-color: rgb(108, =
117, 125); }

.btn-outline-secondary:hover { color: rgb(255, 255, 255); background-color:=
 rgb(108, 117, 125); border-color: rgb(108, 117, 125); }

.btn-outline-secondary.focus, .btn-outline-secondary:focus { box-shadow: rg=
ba(108, 117, 125, 0.5) 0px 0px 0px 0.2rem; }

.btn-outline-secondary.disabled, .btn-outline-secondary:disabled { color: r=
gb(108, 117, 125); background-color: transparent; }

.btn-outline-secondary:not(:disabled):not(.disabled).active, .btn-outline-s=
econdary:not(:disabled):not(.disabled):active, .show > .btn-outline-seconda=
ry.dropdown-toggle { color: rgb(255, 255, 255); background-color: rgb(108, =
117, 125); border-color: rgb(108, 117, 125); }

.btn-outline-secondary:not(:disabled):not(.disabled).active:focus, .btn-out=
line-secondary:not(:disabled):not(.disabled):active:focus, .show > .btn-out=
line-secondary.dropdown-toggle:focus { box-shadow: rgba(108, 117, 125, 0.5)=
 0px 0px 0px 0.2rem; }

.btn-outline-success { color: rgb(40, 167, 69); border-color: rgb(40, 167, =
69); }

.btn-outline-success:hover { color: rgb(255, 255, 255); background-color: r=
gb(40, 167, 69); border-color: rgb(40, 167, 69); }

.btn-outline-success.focus, .btn-outline-success:focus { box-shadow: rgba(4=
0, 167, 69, 0.5) 0px 0px 0px 0.2rem; }

.btn-outline-success.disabled, .btn-outline-success:disabled { color: rgb(4=
0, 167, 69); background-color: transparent; }

.btn-outline-success:not(:disabled):not(.disabled).active, .btn-outline-suc=
cess:not(:disabled):not(.disabled):active, .show > .btn-outline-success.dro=
pdown-toggle { color: rgb(255, 255, 255); background-color: rgb(40, 167, 69=
); border-color: rgb(40, 167, 69); }

.btn-outline-success:not(:disabled):not(.disabled).active:focus, .btn-outli=
ne-success:not(:disabled):not(.disabled):active:focus, .show > .btn-outline=
-success.dropdown-toggle:focus { box-shadow: rgba(40, 167, 69, 0.5) 0px 0px=
 0px 0.2rem; }

.btn-outline-info { color: rgb(23, 162, 184); border-color: rgb(23, 162, 18=
4); }

.btn-outline-info:hover { color: rgb(255, 255, 255); background-color: rgb(=
23, 162, 184); border-color: rgb(23, 162, 184); }

.btn-outline-info.focus, .btn-outline-info:focus { box-shadow: rgba(23, 162=
, 184, 0.5) 0px 0px 0px 0.2rem; }

.btn-outline-info.disabled, .btn-outline-info:disabled { color: rgb(23, 162=
, 184); background-color: transparent; }

.btn-outline-info:not(:disabled):not(.disabled).active, .btn-outline-info:n=
ot(:disabled):not(.disabled):active, .show > .btn-outline-info.dropdown-tog=
gle { color: rgb(255, 255, 255); background-color: rgb(23, 162, 184); borde=
r-color: rgb(23, 162, 184); }

.btn-outline-info:not(:disabled):not(.disabled).active:focus, .btn-outline-=
info:not(:disabled):not(.disabled):active:focus, .show > .btn-outline-info.=
dropdown-toggle:focus { box-shadow: rgba(23, 162, 184, 0.5) 0px 0px 0px 0.2=
rem; }

.btn-outline-warning { color: rgb(255, 193, 7); border-color: rgb(255, 193,=
 7); }

.btn-outline-warning:hover { color: rgb(33, 37, 41); background-color: rgb(=
255, 193, 7); border-color: rgb(255, 193, 7); }

.btn-outline-warning.focus, .btn-outline-warning:focus { box-shadow: rgba(2=
55, 193, 7, 0.5) 0px 0px 0px 0.2rem; }

.btn-outline-warning.disabled, .btn-outline-warning:disabled { color: rgb(2=
55, 193, 7); background-color: transparent; }

.btn-outline-warning:not(:disabled):not(.disabled).active, .btn-outline-war=
ning:not(:disabled):not(.disabled):active, .show > .btn-outline-warning.dro=
pdown-toggle { color: rgb(33, 37, 41); background-color: rgb(255, 193, 7); =
border-color: rgb(255, 193, 7); }

.btn-outline-warning:not(:disabled):not(.disabled).active:focus, .btn-outli=
ne-warning:not(:disabled):not(.disabled):active:focus, .show > .btn-outline=
-warning.dropdown-toggle:focus { box-shadow: rgba(255, 193, 7, 0.5) 0px 0px=
 0px 0.2rem; }

.btn-outline-danger { color: rgb(220, 53, 69); border-color: rgb(220, 53, 6=
9); }

.btn-outline-danger:hover { color: rgb(255, 255, 255); background-color: rg=
b(220, 53, 69); border-color: rgb(220, 53, 69); }

.btn-outline-danger.focus, .btn-outline-danger:focus { box-shadow: rgba(220=
, 53, 69, 0.5) 0px 0px 0px 0.2rem; }

.btn-outline-danger.disabled, .btn-outline-danger:disabled { color: rgb(220=
, 53, 69); background-color: transparent; }

.btn-outline-danger:not(:disabled):not(.disabled).active, .btn-outline-dang=
er:not(:disabled):not(.disabled):active, .show > .btn-outline-danger.dropdo=
wn-toggle { color: rgb(255, 255, 255); background-color: rgb(220, 53, 69); =
border-color: rgb(220, 53, 69); }

.btn-outline-danger:not(:disabled):not(.disabled).active:focus, .btn-outlin=
e-danger:not(:disabled):not(.disabled):active:focus, .show > .btn-outline-d=
anger.dropdown-toggle:focus { box-shadow: rgba(220, 53, 69, 0.5) 0px 0px 0p=
x 0.2rem; }

.btn-outline-light { color: rgb(248, 249, 250); border-color: rgb(248, 249,=
 250); }

.btn-outline-light:hover { color: rgb(33, 37, 41); background-color: rgb(24=
8, 249, 250); border-color: rgb(248, 249, 250); }

.btn-outline-light.focus, .btn-outline-light:focus { box-shadow: rgba(248, =
249, 250, 0.5) 0px 0px 0px 0.2rem; }

.btn-outline-light.disabled, .btn-outline-light:disabled { color: rgb(248, =
249, 250); background-color: transparent; }

.btn-outline-light:not(:disabled):not(.disabled).active, .btn-outline-light=
:not(:disabled):not(.disabled):active, .show > .btn-outline-light.dropdown-=
toggle { color: rgb(33, 37, 41); background-color: rgb(248, 249, 250); bord=
er-color: rgb(248, 249, 250); }

.btn-outline-light:not(:disabled):not(.disabled).active:focus, .btn-outline=
-light:not(:disabled):not(.disabled):active:focus, .show > .btn-outline-lig=
ht.dropdown-toggle:focus { box-shadow: rgba(248, 249, 250, 0.5) 0px 0px 0px=
 0.2rem; }

.btn-outline-dark { color: rgb(52, 58, 64); border-color: rgb(52, 58, 64); =
}

.btn-outline-dark:hover { color: rgb(255, 255, 255); background-color: rgb(=
52, 58, 64); border-color: rgb(52, 58, 64); }

.btn-outline-dark.focus, .btn-outline-dark:focus { box-shadow: rgba(52, 58,=
 64, 0.5) 0px 0px 0px 0.2rem; }

.btn-outline-dark.disabled, .btn-outline-dark:disabled { color: rgb(52, 58,=
 64); background-color: transparent; }

.btn-outline-dark:not(:disabled):not(.disabled).active, .btn-outline-dark:n=
ot(:disabled):not(.disabled):active, .show > .btn-outline-dark.dropdown-tog=
gle { color: rgb(255, 255, 255); background-color: rgb(52, 58, 64); border-=
color: rgb(52, 58, 64); }

.btn-outline-dark:not(:disabled):not(.disabled).active:focus, .btn-outline-=
dark:not(:disabled):not(.disabled):active:focus, .show > .btn-outline-dark.=
dropdown-toggle:focus { box-shadow: rgba(52, 58, 64, 0.5) 0px 0px 0px 0.2re=
m; }

.btn-link { font-weight: 400; color: rgb(0, 123, 255); text-decoration: non=
e; }

.btn-link:hover { color: rgb(0, 86, 179); text-decoration: underline; }

.btn-link.focus, .btn-link:focus { text-decoration: underline; box-shadow: =
none; }

.btn-link.disabled, .btn-link:disabled { color: rgb(108, 117, 125); pointer=
-events: none; }

.btn-group-lg > .btn, .btn-lg { padding: 0.5rem 1rem; font-size: 1.25rem; l=
ine-height: 1.5; border-radius: 0.3rem; }

.btn-group-sm > .btn, .btn-sm { padding: 0.25rem 0.5rem; font-size: 0.875re=
m; line-height: 1.5; border-radius: 0.2rem; }

.btn-block { display: block; width: 100%; }

.btn-block + .btn-block { margin-top: 0.5rem; }

input[type=3D"button"].btn-block, input[type=3D"reset"].btn-block, input[ty=
pe=3D"submit"].btn-block { width: 100%; }

.fade { transition: opacity 0.15s linear 0s; }

@media (prefers-reduced-motion: reduce) {
  .fade { transition: none 0s ease 0s; }
}

.fade:not(.show) { opacity: 0; }

.collapse:not(.show) { display: none; }

.collapsing { position: relative; height: 0px; overflow: hidden; transition=
: height 0.35s ease 0s; }

@media (prefers-reduced-motion: reduce) {
  .collapsing { transition: none 0s ease 0s; }
}

.dropdown, .dropleft, .dropright, .dropup { position: relative; }

.dropdown-toggle { white-space: nowrap; }

.dropdown-toggle::after { display: inline-block; margin-left: 0.255em; vert=
ical-align: 0.255em; content: ""; border-width: 0.3em 0.3em 0px; border-top=
-style: solid; border-top-color: initial; border-right-style: solid; border=
-right-color: transparent; border-bottom-style: initial; border-bottom-colo=
r: initial; border-left-style: solid; border-left-color: transparent; }

.dropdown-toggle:empty::after { margin-left: 0px; }

.dropdown-menu { position: absolute; top: 100%; left: 0px; z-index: 1000; d=
isplay: none; float: left; min-width: 10rem; padding: 0.5rem 0px; margin: 0=
.125rem 0px 0px; font-size: 1rem; color: rgb(33, 37, 41); text-align: left;=
 list-style: none; background-color: rgb(255, 255, 255); background-clip: p=
adding-box; border: 1px solid rgba(0, 0, 0, 0.15); border-radius: 0.25rem; =
}

.dropdown-menu-left { right: auto; left: 0px; }

.dropdown-menu-right { right: 0px; left: auto; }

@media (min-width: 576px) {
  .dropdown-menu-sm-left { right: auto; left: 0px; }
  .dropdown-menu-sm-right { right: 0px; left: auto; }
}

@media (min-width: 768px) {
  .dropdown-menu-md-left { right: auto; left: 0px; }
  .dropdown-menu-md-right { right: 0px; left: auto; }
}

@media (min-width: 992px) {
  .dropdown-menu-lg-left { right: auto; left: 0px; }
  .dropdown-menu-lg-right { right: 0px; left: auto; }
}

@media (min-width: 1200px) {
  .dropdown-menu-xl-left { right: auto; left: 0px; }
  .dropdown-menu-xl-right { right: 0px; left: auto; }
}

.dropup .dropdown-menu { top: auto; bottom: 100%; margin-top: 0px; margin-b=
ottom: 0.125rem; }

.dropup .dropdown-toggle::after { display: inline-block; margin-left: 0.255=
em; vertical-align: 0.255em; content: ""; border-width: 0px 0.3em 0.3em; bo=
rder-top-style: initial; border-top-color: initial; border-right-style: sol=
id; border-right-color: transparent; border-bottom-style: solid; border-bot=
tom-color: initial; border-left-style: solid; border-left-color: transparen=
t; }

.dropup .dropdown-toggle:empty::after { margin-left: 0px; }

.dropright .dropdown-menu { top: 0px; right: auto; left: 100%; margin-top: =
0px; margin-left: 0.125rem; }

.dropright .dropdown-toggle::after { display: inline-block; margin-left: 0.=
255em; vertical-align: 0.255em; content: ""; border-width: 0.3em 0px 0.3em =
0.3em; border-top-style: solid; border-top-color: transparent; border-right=
-style: initial; border-right-color: initial; border-bottom-style: solid; b=
order-bottom-color: transparent; border-left-style: solid; border-left-colo=
r: initial; }

.dropright .dropdown-toggle:empty::after { margin-left: 0px; }

.dropright .dropdown-toggle::after { vertical-align: 0px; }

.dropleft .dropdown-menu { top: 0px; right: 100%; left: auto; margin-top: 0=
px; margin-right: 0.125rem; }

.dropleft .dropdown-toggle::after { display: inline-block; margin-left: 0.2=
55em; vertical-align: 0.255em; content: ""; }

.dropleft .dropdown-toggle::after { display: none; }

.dropleft .dropdown-toggle::before { display: inline-block; margin-right: 0=
.255em; vertical-align: 0.255em; content: ""; border-top: 0.3em solid trans=
parent; border-right: 0.3em solid; border-bottom: 0.3em solid transparent; =
}

.dropleft .dropdown-toggle:empty::after { margin-left: 0px; }

.dropleft .dropdown-toggle::before { vertical-align: 0px; }

.dropdown-menu[x-placement^=3D"bottom"], .dropdown-menu[x-placement^=3D"lef=
t"], .dropdown-menu[x-placement^=3D"right"], .dropdown-menu[x-placement^=3D=
"top"] { right: auto; bottom: auto; }

.dropdown-divider { height: 0px; margin: 0.5rem 0px; overflow: hidden; bord=
er-top: 1px solid rgb(233, 236, 239); }

.dropdown-item { display: block; width: 100%; padding: 0.25rem 1.5rem; clea=
r: both; font-weight: 400; color: rgb(33, 37, 41); text-align: inherit; whi=
te-space: nowrap; background-color: transparent; border: 0px; }

.dropdown-item:focus, .dropdown-item:hover { color: rgb(22, 24, 27); text-d=
ecoration: none; background-color: rgb(248, 249, 250); }

.dropdown-item.active, .dropdown-item:active { color: rgb(255, 255, 255); t=
ext-decoration: none; background-color: rgb(0, 123, 255); }

.dropdown-item.disabled, .dropdown-item:disabled { color: rgb(108, 117, 125=
); pointer-events: none; background-color: transparent; }

.dropdown-menu.show { display: block; }

.dropdown-header { display: block; padding: 0.5rem 1.5rem; margin-bottom: 0=
px; font-size: 0.875rem; color: rgb(108, 117, 125); white-space: nowrap; }

.dropdown-item-text { display: block; padding: 0.25rem 1.5rem; color: rgb(3=
3, 37, 41); }

.btn-group, .btn-group-vertical { position: relative; display: inline-flex;=
 vertical-align: middle; }

.btn-group-vertical > .btn, .btn-group > .btn { position: relative; flex: 1=
 1 auto; }

.btn-group-vertical > .btn:hover, .btn-group > .btn:hover { z-index: 1; }

.btn-group-vertical > .btn.active, .btn-group-vertical > .btn:active, .btn-=
group-vertical > .btn:focus, .btn-group > .btn.active, .btn-group > .btn:ac=
tive, .btn-group > .btn:focus { z-index: 1; }

.btn-toolbar { display: flex; flex-wrap: wrap; justify-content: flex-start;=
 }

.btn-toolbar .input-group { width: auto; }

.btn-group > .btn-group:not(:first-child), .btn-group > .btn:not(:first-chi=
ld) { margin-left: -1px; }

.btn-group > .btn-group:not(:last-child) > .btn, .btn-group > .btn:not(:las=
t-child):not(.dropdown-toggle) { border-top-right-radius: 0px; border-botto=
m-right-radius: 0px; }

.btn-group > .btn-group:not(:first-child) > .btn, .btn-group > .btn:not(:fi=
rst-child) { border-top-left-radius: 0px; border-bottom-left-radius: 0px; }

.dropdown-toggle-split { padding-right: 0.5625rem; padding-left: 0.5625rem;=
 }

.dropdown-toggle-split::after, .dropright .dropdown-toggle-split::after, .d=
ropup .dropdown-toggle-split::after { margin-left: 0px; }

.dropleft .dropdown-toggle-split::before { margin-right: 0px; }

.btn-group-sm > .btn + .dropdown-toggle-split, .btn-sm + .dropdown-toggle-s=
plit { padding-right: 0.375rem; padding-left: 0.375rem; }

.btn-group-lg > .btn + .dropdown-toggle-split, .btn-lg + .dropdown-toggle-s=
plit { padding-right: 0.75rem; padding-left: 0.75rem; }

.btn-group-vertical { flex-direction: column; align-items: flex-start; just=
ify-content: center; }

.btn-group-vertical > .btn, .btn-group-vertical > .btn-group { width: 100%;=
 }

.btn-group-vertical > .btn-group:not(:first-child), .btn-group-vertical > .=
btn:not(:first-child) { margin-top: -1px; }

.btn-group-vertical > .btn-group:not(:last-child) > .btn, .btn-group-vertic=
al > .btn:not(:last-child):not(.dropdown-toggle) { border-bottom-right-radi=
us: 0px; border-bottom-left-radius: 0px; }

.btn-group-vertical > .btn-group:not(:first-child) > .btn, .btn-group-verti=
cal > .btn:not(:first-child) { border-top-left-radius: 0px; border-top-righ=
t-radius: 0px; }

.btn-group-toggle > .btn, .btn-group-toggle > .btn-group > .btn { margin-bo=
ttom: 0px; }

.btn-group-toggle > .btn input[type=3D"checkbox"], .btn-group-toggle > .btn=
 input[type=3D"radio"], .btn-group-toggle > .btn-group > .btn input[type=3D=
"checkbox"], .btn-group-toggle > .btn-group > .btn input[type=3D"radio"] { =
position: absolute; clip: rect(0px, 0px, 0px, 0px); pointer-events: none; }

.input-group { position: relative; display: flex; flex-wrap: wrap; align-it=
ems: stretch; width: 100%; }

.input-group > .custom-file, .input-group > .custom-select, .input-group > =
.form-control, .input-group > .form-control-plaintext { position: relative;=
 flex: 1 1 auto; width: 1%; margin-bottom: 0px; }

.input-group > .custom-file + .custom-file, .input-group > .custom-file + .=
custom-select, .input-group > .custom-file + .form-control, .input-group > =
.custom-select + .custom-file, .input-group > .custom-select + .custom-sele=
ct, .input-group > .custom-select + .form-control, .input-group > .form-con=
trol + .custom-file, .input-group > .form-control + .custom-select, .input-=
group > .form-control + .form-control, .input-group > .form-control-plainte=
xt + .custom-file, .input-group > .form-control-plaintext + .custom-select,=
 .input-group > .form-control-plaintext + .form-control { margin-left: -1px=
; }

.input-group > .custom-file .custom-file-input:focus ~ .custom-file-label, =
.input-group > .custom-select:focus, .input-group > .form-control:focus { z=
-index: 3; }

.input-group > .custom-file .custom-file-input:focus { z-index: 4; }

.input-group > .custom-select:not(:last-child), .input-group > .form-contro=
l:not(:last-child) { border-top-right-radius: 0px; border-bottom-right-radi=
us: 0px; }

.input-group > .custom-select:not(:first-child), .input-group > .form-contr=
ol:not(:first-child) { border-top-left-radius: 0px; border-bottom-left-radi=
us: 0px; }

.input-group > .custom-file { display: flex; align-items: center; }

.input-group > .custom-file:not(:last-child) .custom-file-label, .input-gro=
up > .custom-file:not(:last-child) .custom-file-label::after { border-top-r=
ight-radius: 0px; border-bottom-right-radius: 0px; }

.input-group > .custom-file:not(:first-child) .custom-file-label { border-t=
op-left-radius: 0px; border-bottom-left-radius: 0px; }

.input-group-append, .input-group-prepend { display: flex; }

.input-group-append .btn, .input-group-prepend .btn { position: relative; z=
-index: 2; }

.input-group-append .btn:focus, .input-group-prepend .btn:focus { z-index: =
3; }

.input-group-append .btn + .btn, .input-group-append .btn + .input-group-te=
xt, .input-group-append .input-group-text + .btn, .input-group-append .inpu=
t-group-text + .input-group-text, .input-group-prepend .btn + .btn, .input-=
group-prepend .btn + .input-group-text, .input-group-prepend .input-group-t=
ext + .btn, .input-group-prepend .input-group-text + .input-group-text { ma=
rgin-left: -1px; }

.input-group-prepend { margin-right: -1px; }

.input-group-append { margin-left: -1px; }

.input-group-text { display: flex; align-items: center; padding: 0.375rem 0=
.75rem; margin-bottom: 0px; font-size: 1rem; font-weight: 400; line-height:=
 1.5; color: rgb(73, 80, 87); text-align: center; white-space: nowrap; back=
ground-color: rgb(233, 236, 239); border: 1px solid rgb(206, 212, 218); bor=
der-radius: 0.25rem; }

.input-group-text input[type=3D"checkbox"], .input-group-text input[type=3D=
"radio"] { margin-top: 0px; }

.input-group-lg > .custom-select, .input-group-lg > .form-control:not(texta=
rea) { height: calc(1.5em + 1rem + 2px); }

.input-group-lg > .custom-select, .input-group-lg > .form-control, .input-g=
roup-lg > .input-group-append > .btn, .input-group-lg > .input-group-append=
 > .input-group-text, .input-group-lg > .input-group-prepend > .btn, .input=
-group-lg > .input-group-prepend > .input-group-text { padding: 0.5rem 1rem=
; font-size: 1.25rem; line-height: 1.5; border-radius: 0.3rem; }

.input-group-sm > .custom-select, .input-group-sm > .form-control:not(texta=
rea) { height: calc(1.5em + 0.5rem + 2px); }

.input-group-sm > .custom-select, .input-group-sm > .form-control, .input-g=
roup-sm > .input-group-append > .btn, .input-group-sm > .input-group-append=
 > .input-group-text, .input-group-sm > .input-group-prepend > .btn, .input=
-group-sm > .input-group-prepend > .input-group-text { padding: 0.25rem 0.5=
rem; font-size: 0.875rem; line-height: 1.5; border-radius: 0.2rem; }

.input-group-lg > .custom-select, .input-group-sm > .custom-select { paddin=
g-right: 1.75rem; }

.input-group > .input-group-append:last-child > .btn:not(:last-child):not(.=
dropdown-toggle), .input-group > .input-group-append:last-child > .input-gr=
oup-text:not(:last-child), .input-group > .input-group-append:not(:last-chi=
ld) > .btn, .input-group > .input-group-append:not(:last-child) > .input-gr=
oup-text, .input-group > .input-group-prepend > .btn, .input-group > .input=
-group-prepend > .input-group-text { border-top-right-radius: 0px; border-b=
ottom-right-radius: 0px; }

.input-group > .input-group-append > .btn, .input-group > .input-group-appe=
nd > .input-group-text, .input-group > .input-group-prepend:first-child > .=
btn:not(:first-child), .input-group > .input-group-prepend:first-child > .i=
nput-group-text:not(:first-child), .input-group > .input-group-prepend:not(=
:first-child) > .btn, .input-group > .input-group-prepend:not(:first-child)=
 > .input-group-text { border-top-left-radius: 0px; border-bottom-left-radi=
us: 0px; }

.custom-control { position: relative; display: block; min-height: 1.5rem; p=
adding-left: 1.5rem; }

.custom-control-inline { display: inline-flex; margin-right: 1rem; }

.custom-control-input { position: absolute; z-index: -1; opacity: 0; }

.custom-control-input:checked ~ .custom-control-label::before { color: rgb(=
255, 255, 255); border-color: rgb(0, 123, 255); background-color: rgb(0, 12=
3, 255); }

.custom-control-input:focus ~ .custom-control-label::before { box-shadow: r=
gba(0, 123, 255, 0.25) 0px 0px 0px 0.2rem; }

.custom-control-input:focus:not(:checked) ~ .custom-control-label::before {=
 border-color: rgb(128, 189, 255); }

.custom-control-input:not(:disabled):active ~ .custom-control-label::before=
 { color: rgb(255, 255, 255); background-color: rgb(179, 215, 255); border-=
color: rgb(179, 215, 255); }

.custom-control-input:disabled ~ .custom-control-label { color: rgb(108, 11=
7, 125); }

.custom-control-input:disabled ~ .custom-control-label::before { background=
-color: rgb(233, 236, 239); }

.custom-control-label { position: relative; margin-bottom: 0px; vertical-al=
ign: top; }

.custom-control-label::before { position: absolute; top: 0.25rem; left: -1.=
5rem; display: block; width: 1rem; height: 1rem; pointer-events: none; cont=
ent: ""; background-color: rgb(255, 255, 255); border: 1px solid rgb(173, 1=
81, 189); }

.custom-control-label::after { position: absolute; top: 0.25rem; left: -1.5=
rem; display: block; width: 1rem; height: 1rem; content: ""; background: 50=
% center / 50% 50% no-repeat; }

.custom-checkbox .custom-control-label::before { border-radius: 0.25rem; }

.custom-checkbox .custom-control-input:checked ~ .custom-control-label::aft=
er { background-image: url("data:image/svg+xml,%3csvg xmlns=3D'http://www.w=
3.org/2000/svg' viewBox=3D'0 0 8 8'%3e%3cpath fill=3D'%23fff' d=3D'M6.564.7=
5l-3.59 3.612-1.538-1.55L0 4.26 2.974 7.25 8 2.193z'/%3e%3c/svg%3e"); }

.custom-checkbox .custom-control-input:indeterminate ~ .custom-control-labe=
l::before { border-color: rgb(0, 123, 255); background-color: rgb(0, 123, 2=
55); }

.custom-checkbox .custom-control-input:indeterminate ~ .custom-control-labe=
l::after { background-image: url("data:image/svg+xml,%3csvg xmlns=3D'http:/=
/www.w3.org/2000/svg' viewBox=3D'0 0 4 4'%3e%3cpath stroke=3D'%23fff' d=3D'=
M0 2h4'/%3e%3c/svg%3e"); }

.custom-checkbox .custom-control-input:disabled:checked ~ .custom-control-l=
abel::before { background-color: rgba(0, 123, 255, 0.5); }

.custom-checkbox .custom-control-input:disabled:indeterminate ~ .custom-con=
trol-label::before { background-color: rgba(0, 123, 255, 0.5); }

.custom-radio .custom-control-label::before { border-radius: 50%; }

.custom-radio .custom-control-input:checked ~ .custom-control-label::after =
{ background-image: url("data:image/svg+xml,%3csvg xmlns=3D'http://www.w3.o=
rg/2000/svg' viewBox=3D'-4 -4 8 8'%3e%3ccircle r=3D'3' fill=3D'%23fff'/%3e%=
3c/svg%3e"); }

.custom-radio .custom-control-input:disabled:checked ~ .custom-control-labe=
l::before { background-color: rgba(0, 123, 255, 0.5); }

.custom-switch { padding-left: 2.25rem; }

.custom-switch .custom-control-label::before { left: -2.25rem; width: 1.75r=
em; pointer-events: all; border-radius: 0.5rem; }

.custom-switch .custom-control-label::after { top: calc(0.25rem + 2px); lef=
t: calc(-2.25rem + 2px); width: calc(1rem - 4px); height: calc(1rem - 4px);=
 background-color: rgb(173, 181, 189); border-radius: 0.5rem; transition: t=
ransform 0.15s ease-in-out 0s, background-color 0.15s ease-in-out 0s, borde=
r-color 0.15s ease-in-out 0s, box-shadow 0.15s ease-in-out 0s, -webkit-tran=
sform 0.15s ease-in-out 0s; }

@media (prefers-reduced-motion: reduce) {
  .custom-switch .custom-control-label::after { transition: none 0s ease 0s=
; }
}

.custom-switch .custom-control-input:checked ~ .custom-control-label::after=
 { background-color: rgb(255, 255, 255); transform: translateX(0.75rem); }

.custom-switch .custom-control-input:disabled:checked ~ .custom-control-lab=
el::before { background-color: rgba(0, 123, 255, 0.5); }

.custom-select { display: inline-block; width: 100%; height: calc(1.5em + 0=
.75rem + 2px); padding: 0.375rem 1.75rem 0.375rem 0.75rem; font-size: 1rem;=
 font-weight: 400; line-height: 1.5; color: rgb(73, 80, 87); vertical-align=
: middle; background: url("data:image/svg+xml,%3csvg xmlns=3D'http://www.w3=
.org/2000/svg' viewBox=3D'0 0 4 5'%3e%3cpath fill=3D'%23343a40' d=3D'M2 0L0=
 2h4zm0 5L0 3h4z'/%3e%3c/svg%3e") right 0.75rem center / 8px 10px no-repeat=
 rgb(255, 255, 255); border: 1px solid rgb(206, 212, 218); border-radius: 0=
.25rem; appearance: none; }

.custom-select:focus { border-color: rgb(128, 189, 255); outline: 0px; box-=
shadow: rgba(0, 123, 255, 0.25) 0px 0px 0px 0.2rem; }

.custom-select[multiple], .custom-select[size]:not([size=3D"1"]) { height: =
auto; padding-right: 0.75rem; background-image: none; }

.custom-select:disabled { color: rgb(108, 117, 125); background-color: rgb(=
233, 236, 239); }

.custom-select-sm { height: calc(1.5em + 0.5rem + 2px); padding-top: 0.25re=
m; padding-bottom: 0.25rem; padding-left: 0.5rem; font-size: 0.875rem; }

.custom-select-lg { height: calc(1.5em + 1rem + 2px); padding-top: 0.5rem; =
padding-bottom: 0.5rem; padding-left: 1rem; font-size: 1.25rem; }

.custom-file { position: relative; display: inline-block; width: 100%; heig=
ht: calc(1.5em + 0.75rem + 2px); margin-bottom: 0px; }

.custom-file-input { position: relative; z-index: 2; width: 100%; height: c=
alc(1.5em + 0.75rem + 2px); margin: 0px; opacity: 0; }

.custom-file-input:focus ~ .custom-file-label { border-color: rgb(128, 189,=
 255); box-shadow: rgba(0, 123, 255, 0.25) 0px 0px 0px 0.2rem; }

.custom-file-input:disabled ~ .custom-file-label { background-color: rgb(23=
3, 236, 239); }

.custom-file-input:lang(en) ~ .custom-file-label::after { content: "Browse"=
; }

.custom-file-input ~ .custom-file-label[data-browse]::after { content: attr=
(data-browse); }

.custom-file-label { position: absolute; top: 0px; right: 0px; left: 0px; z=
-index: 1; height: calc(1.5em + 0.75rem + 2px); padding: 0.375rem 0.75rem; =
font-weight: 400; line-height: 1.5; color: rgb(73, 80, 87); background-colo=
r: rgb(255, 255, 255); border: 1px solid rgb(206, 212, 218); border-radius:=
 0.25rem; }

.custom-file-label::after { position: absolute; top: 0px; right: 0px; botto=
m: 0px; z-index: 3; display: block; height: calc(1.5em + 0.75rem); padding:=
 0.375rem 0.75rem; line-height: 1.5; color: rgb(73, 80, 87); content: "Brow=
se"; background-color: rgb(233, 236, 239); border-left: inherit; border-rad=
ius: 0px 0.25rem 0.25rem 0px; }

.custom-range { width: 100%; height: calc(1.4rem); padding: 0px; background=
-color: transparent; appearance: none; }

.custom-range:focus { outline: 0px; }

.custom-range:focus::-webkit-slider-thumb { box-shadow: rgb(255, 255, 255) =
0px 0px 0px 1px, rgba(0, 123, 255, 0.25) 0px 0px 0px 0.2rem; }

.custom-range::-webkit-slider-thumb { width: 1rem; height: 1rem; margin-top=
: -0.25rem; background-color: rgb(0, 123, 255); border: 0px; border-radius:=
 1rem; transition: background-color 0.15s ease-in-out 0s, border-color 0.15=
s ease-in-out 0s, box-shadow 0.15s ease-in-out 0s; appearance: none; }

@media (prefers-reduced-motion: reduce) {
  .custom-range::-webkit-slider-thumb { transition: none 0s ease 0s; }
}

.custom-range::-webkit-slider-thumb:active { background-color: rgb(179, 215=
, 255); }

.custom-range::-webkit-slider-runnable-track { width: 100%; height: 0.5rem;=
 color: transparent; cursor: pointer; background-color: rgb(222, 226, 230);=
 border-color: transparent; border-radius: 1rem; }

@media (prefers-reduced-motion: reduce) {
}

@media (prefers-reduced-motion: reduce) {
}

.custom-range:disabled::-webkit-slider-thumb { background-color: rgb(173, 1=
81, 189); }

.custom-range:disabled::-webkit-slider-runnable-track { cursor: default; }

.custom-control-label::before, .custom-file-label, .custom-select { transit=
ion: background-color 0.15s ease-in-out 0s, border-color 0.15s ease-in-out =
0s, box-shadow 0.15s ease-in-out 0s; }

@media (prefers-reduced-motion: reduce) {
  .custom-control-label::before, .custom-file-label, .custom-select { trans=
ition: none 0s ease 0s; }
}

.nav { display: flex; flex-wrap: wrap; padding-left: 0px; margin-bottom: 0p=
x; list-style: none; }

.nav-link { display: block; padding: 0.5rem 1rem; }

.nav-link:focus, .nav-link:hover { text-decoration: none; }

.nav-link.disabled { color: rgb(108, 117, 125); pointer-events: none; curso=
r: default; }

.nav-tabs { border-bottom: 1px solid rgb(222, 226, 230); }

.nav-tabs .nav-item { margin-bottom: -1px; }

.nav-tabs .nav-link { border: 1px solid transparent; border-top-left-radius=
: 0.25rem; border-top-right-radius: 0.25rem; }

.nav-tabs .nav-link:focus, .nav-tabs .nav-link:hover { border-color: rgb(23=
3, 236, 239) rgb(233, 236, 239) rgb(222, 226, 230); }

.nav-tabs .nav-link.disabled { color: rgb(108, 117, 125); background-color:=
 transparent; border-color: transparent; }

.nav-tabs .nav-item.show .nav-link, .nav-tabs .nav-link.active { color: rgb=
(73, 80, 87); background-color: rgb(255, 255, 255); border-color: rgb(222, =
226, 230) rgb(222, 226, 230) rgb(255, 255, 255); }

.nav-tabs .dropdown-menu { margin-top: -1px; border-top-left-radius: 0px; b=
order-top-right-radius: 0px; }

.nav-pills .nav-link { border-radius: 0.25rem; }

.nav-pills .nav-link.active, .nav-pills .show > .nav-link { color: rgb(255,=
 255, 255); background-color: rgb(0, 123, 255); }

.nav-fill .nav-item { flex: 1 1 auto; text-align: center; }

.nav-justified .nav-item { flex-basis: 0px; flex-grow: 1; text-align: cente=
r; }

.tab-content > .tab-pane { display: none; }

.tab-content > .active { display: block; }

.navbar { position: relative; display: flex; flex-wrap: wrap; align-items: =
center; justify-content: space-between; padding: 0.5rem 1rem; }

.navbar > .container, .navbar > .container-fluid { display: flex; flex-wrap=
: wrap; align-items: center; justify-content: space-between; }

.navbar-brand { display: inline-block; padding-top: 0.3125rem; padding-bott=
om: 0.3125rem; margin-right: 1rem; font-size: 1.25rem; line-height: inherit=
; white-space: nowrap; }

.navbar-brand:focus, .navbar-brand:hover { text-decoration: none; }

.navbar-nav { display: flex; flex-direction: column; padding-left: 0px; mar=
gin-bottom: 0px; list-style: none; }

.navbar-nav .nav-link { padding-right: 0px; padding-left: 0px; }

.navbar-nav .dropdown-menu { position: static; float: none; }

.navbar-text { display: inline-block; padding-top: 0.5rem; padding-bottom: =
0.5rem; }

.navbar-collapse { flex-basis: 100%; flex-grow: 1; align-items: center; }

.navbar-toggler { padding: 0.25rem 0.75rem; font-size: 1.25rem; line-height=
: 1; background-color: transparent; border: 1px solid transparent; border-r=
adius: 0.25rem; }

.navbar-toggler:focus, .navbar-toggler:hover { text-decoration: none; }

.navbar-toggler-icon { display: inline-block; width: 1.5em; height: 1.5em; =
vertical-align: middle; content: ""; background: center center / 100% 100% =
no-repeat; }

@media (max-width: 575.98px) {
  .navbar-expand-sm > .container, .navbar-expand-sm > .container-fluid { pa=
dding-right: 0px; padding-left: 0px; }
}

@media (min-width: 576px) {
  .navbar-expand-sm { flex-flow: row nowrap; justify-content: flex-start; }
  .navbar-expand-sm .navbar-nav { flex-direction: row; }
  .navbar-expand-sm .navbar-nav .dropdown-menu { position: absolute; }
  .navbar-expand-sm .navbar-nav .nav-link { padding-right: 0.5rem; padding-=
left: 0.5rem; }
  .navbar-expand-sm > .container, .navbar-expand-sm > .container-fluid { fl=
ex-wrap: nowrap; }
  .navbar-expand-sm .navbar-collapse { flex-basis: auto; display: flex !imp=
ortant; }
  .navbar-expand-sm .navbar-toggler { display: none; }
}

@media (max-width: 767.98px) {
  .navbar-expand-md > .container, .navbar-expand-md > .container-fluid { pa=
dding-right: 0px; padding-left: 0px; }
}

@media (min-width: 768px) {
  .navbar-expand-md { flex-flow: row nowrap; justify-content: flex-start; }
  .navbar-expand-md .navbar-nav { flex-direction: row; }
  .navbar-expand-md .navbar-nav .dropdown-menu { position: absolute; }
  .navbar-expand-md .navbar-nav .nav-link { padding-right: 0.5rem; padding-=
left: 0.5rem; }
  .navbar-expand-md > .container, .navbar-expand-md > .container-fluid { fl=
ex-wrap: nowrap; }
  .navbar-expand-md .navbar-collapse { flex-basis: auto; display: flex !imp=
ortant; }
  .navbar-expand-md .navbar-toggler { display: none; }
}

@media (max-width: 991.98px) {
  .navbar-expand-lg > .container, .navbar-expand-lg > .container-fluid { pa=
dding-right: 0px; padding-left: 0px; }
}

@media (min-width: 992px) {
  .navbar-expand-lg { flex-flow: row nowrap; justify-content: flex-start; }
  .navbar-expand-lg .navbar-nav { flex-direction: row; }
  .navbar-expand-lg .navbar-nav .dropdown-menu { position: absolute; }
  .navbar-expand-lg .navbar-nav .nav-link { padding-right: 0.5rem; padding-=
left: 0.5rem; }
  .navbar-expand-lg > .container, .navbar-expand-lg > .container-fluid { fl=
ex-wrap: nowrap; }
  .navbar-expand-lg .navbar-collapse { flex-basis: auto; display: flex !imp=
ortant; }
  .navbar-expand-lg .navbar-toggler { display: none; }
}

@media (max-width: 1199.98px) {
  .navbar-expand-xl > .container, .navbar-expand-xl > .container-fluid { pa=
dding-right: 0px; padding-left: 0px; }
}

@media (min-width: 1200px) {
  .navbar-expand-xl { flex-flow: row nowrap; justify-content: flex-start; }
  .navbar-expand-xl .navbar-nav { flex-direction: row; }
  .navbar-expand-xl .navbar-nav .dropdown-menu { position: absolute; }
  .navbar-expand-xl .navbar-nav .nav-link { padding-right: 0.5rem; padding-=
left: 0.5rem; }
  .navbar-expand-xl > .container, .navbar-expand-xl > .container-fluid { fl=
ex-wrap: nowrap; }
  .navbar-expand-xl .navbar-collapse { flex-basis: auto; display: flex !imp=
ortant; }
  .navbar-expand-xl .navbar-toggler { display: none; }
}

.navbar-expand { flex-flow: row nowrap; justify-content: flex-start; }

.navbar-expand > .container, .navbar-expand > .container-fluid { padding-ri=
ght: 0px; padding-left: 0px; }

.navbar-expand .navbar-nav { flex-direction: row; }

.navbar-expand .navbar-nav .dropdown-menu { position: absolute; }

.navbar-expand .navbar-nav .nav-link { padding-right: 0.5rem; padding-left:=
 0.5rem; }

.navbar-expand > .container, .navbar-expand > .container-fluid { flex-wrap:=
 nowrap; }

.navbar-expand .navbar-collapse { flex-basis: auto; display: flex !importan=
t; }

.navbar-expand .navbar-toggler { display: none; }

.navbar-light .navbar-brand { color: rgba(0, 0, 0, 0.9); }

.navbar-light .navbar-brand:focus, .navbar-light .navbar-brand:hover { colo=
r: rgba(0, 0, 0, 0.9); }

.navbar-light .navbar-nav .nav-link { color: rgba(0, 0, 0, 0.5); }

.navbar-light .navbar-nav .nav-link:focus, .navbar-light .navbar-nav .nav-l=
ink:hover { color: rgba(0, 0, 0, 0.7); }

.navbar-light .navbar-nav .nav-link.disabled { color: rgba(0, 0, 0, 0.3); }

.navbar-light .navbar-nav .active > .nav-link, .navbar-light .navbar-nav .n=
av-link.active, .navbar-light .navbar-nav .nav-link.show, .navbar-light .na=
vbar-nav .show > .nav-link { color: rgba(0, 0, 0, 0.9); }

.navbar-light .navbar-toggler { color: rgba(0, 0, 0, 0.5); border-color: rg=
ba(0, 0, 0, 0.1); }

.navbar-light .navbar-toggler-icon { background-image: url("data:image/svg+=
xml,%3csvg viewBox=3D'0 0 30 30' xmlns=3D'http://www.w3.org/2000/svg'%3e%3c=
path stroke=3D'rgba(0, 0, 0, 0.5)' stroke-width=3D'2' stroke-linecap=3D'rou=
nd' stroke-miterlimit=3D'10' d=3D'M4 7h22M4 15h22M4 23h22'/%3e%3c/svg%3e");=
 }

.navbar-light .navbar-text { color: rgba(0, 0, 0, 0.5); }

.navbar-light .navbar-text a { color: rgba(0, 0, 0, 0.9); }

.navbar-light .navbar-text a:focus, .navbar-light .navbar-text a:hover { co=
lor: rgba(0, 0, 0, 0.9); }

.navbar-dark .navbar-brand { color: rgb(255, 255, 255); }

.navbar-dark .navbar-brand:focus, .navbar-dark .navbar-brand:hover { color:=
 rgb(255, 255, 255); }

.navbar-dark .navbar-nav .nav-link { color: rgba(255, 255, 255, 0.5); }

.navbar-dark .navbar-nav .nav-link:focus, .navbar-dark .navbar-nav .nav-lin=
k:hover { color: rgba(255, 255, 255, 0.75); }

.navbar-dark .navbar-nav .nav-link.disabled { color: rgba(255, 255, 255, 0.=
25); }

.navbar-dark .navbar-nav .active > .nav-link, .navbar-dark .navbar-nav .nav=
-link.active, .navbar-dark .navbar-nav .nav-link.show, .navbar-dark .navbar=
-nav .show > .nav-link { color: rgb(255, 255, 255); }

.navbar-dark .navbar-toggler { color: rgba(255, 255, 255, 0.5); border-colo=
r: rgba(255, 255, 255, 0.1); }

.navbar-dark .navbar-toggler-icon { background-image: url("data:image/svg+x=
ml,%3csvg viewBox=3D'0 0 30 30' xmlns=3D'http://www.w3.org/2000/svg'%3e%3cp=
ath stroke=3D'rgba(255, 255, 255, 0.5)' stroke-width=3D'2' stroke-linecap=
=3D'round' stroke-miterlimit=3D'10' d=3D'M4 7h22M4 15h22M4 23h22'/%3e%3c/sv=
g%3e"); }

.navbar-dark .navbar-text { color: rgba(255, 255, 255, 0.5); }

.navbar-dark .navbar-text a { color: rgb(255, 255, 255); }

.navbar-dark .navbar-text a:focus, .navbar-dark .navbar-text a:hover { colo=
r: rgb(255, 255, 255); }

.card { position: relative; display: flex; flex-direction: column; min-widt=
h: 0px; overflow-wrap: break-word; background-color: rgb(255, 255, 255); ba=
ckground-clip: border-box; border: 1px solid rgba(0, 0, 0, 0.125); border-r=
adius: 0.25rem; }

.card > hr { margin-right: 0px; margin-left: 0px; }

.card > .list-group:first-child .list-group-item:first-child { border-top-l=
eft-radius: 0.25rem; border-top-right-radius: 0.25rem; }

.card > .list-group:last-child .list-group-item:last-child { border-bottom-=
right-radius: 0.25rem; border-bottom-left-radius: 0.25rem; }

.card-body { flex: 1 1 auto; padding: 1.25rem; }

.card-title { margin-bottom: 0.75rem; }

.card-subtitle { margin-top: -0.375rem; margin-bottom: 0px; }

.card-text:last-child { margin-bottom: 0px; }

.card-link:hover { text-decoration: none; }

.card-link + .card-link { margin-left: 1.25rem; }

.card-header { padding: 0.75rem 1.25rem; margin-bottom: 0px; background-col=
or: rgba(0, 0, 0, 0.03); border-bottom: 1px solid rgba(0, 0, 0, 0.125); }

.card-header:first-child { border-radius: calc(0.25rem - 1px) calc(0.25rem =
- 1px) 0px 0px; }

.card-header + .list-group .list-group-item:first-child { border-top: 0px; =
}

.card-footer { padding: 0.75rem 1.25rem; background-color: rgba(0, 0, 0, 0.=
03); border-top: 1px solid rgba(0, 0, 0, 0.125); }

.card-footer:last-child { border-radius: 0px 0px calc(0.25rem - 1px) calc(0=
.25rem - 1px); }

.card-header-tabs { margin-right: -0.625rem; margin-bottom: -0.75rem; margi=
n-left: -0.625rem; border-bottom: 0px; }

.card-header-pills { margin-right: -0.625rem; margin-left: -0.625rem; }

.card-img-overlay { position: absolute; inset: 0px; padding: 1.25rem; }

.card-img { width: 100%; border-radius: calc(0.25rem - 1px); }

.card-img-top { width: 100%; border-top-left-radius: calc(0.25rem - 1px); b=
order-top-right-radius: calc(0.25rem - 1px); }

.card-img-bottom { width: 100%; border-bottom-right-radius: calc(0.25rem - =
1px); border-bottom-left-radius: calc(0.25rem - 1px); }

.card-deck { display: flex; flex-direction: column; }

.card-deck .card { margin-bottom: 15px; }

@media (min-width: 576px) {
  .card-deck { flex-flow: row wrap; margin-right: -15px; margin-left: -15px=
; }
  .card-deck .card { display: flex; flex: 1 0 0%; flex-direction: column; m=
argin-right: 15px; margin-bottom: 0px; margin-left: 15px; }
}

.card-group { display: flex; flex-direction: column; }

.card-group > .card { margin-bottom: 15px; }

@media (min-width: 576px) {
  .card-group { flex-flow: row wrap; }
  .card-group > .card { flex: 1 0 0%; margin-bottom: 0px; }
  .card-group > .card + .card { margin-left: 0px; border-left: 0px; }
  .card-group > .card:not(:last-child) { border-top-right-radius: 0px; bord=
er-bottom-right-radius: 0px; }
  .card-group > .card:not(:last-child) .card-header, .card-group > .card:no=
t(:last-child) .card-img-top { border-top-right-radius: 0px; }
  .card-group > .card:not(:last-child) .card-footer, .card-group > .card:no=
t(:last-child) .card-img-bottom { border-bottom-right-radius: 0px; }
  .card-group > .card:not(:first-child) { border-top-left-radius: 0px; bord=
er-bottom-left-radius: 0px; }
  .card-group > .card:not(:first-child) .card-header, .card-group > .card:n=
ot(:first-child) .card-img-top { border-top-left-radius: 0px; }
  .card-group > .card:not(:first-child) .card-footer, .card-group > .card:n=
ot(:first-child) .card-img-bottom { border-bottom-left-radius: 0px; }
}

.card-columns .card { margin-bottom: 0.75rem; }

@media (min-width: 576px) {
  .card-columns { column-count: 3; column-gap: 1.25rem; orphans: 1; widows:=
 1; }
  .card-columns .card { display: inline-block; width: 100%; }
}

.accordion > .card { overflow: hidden; }

.accordion > .card:not(:first-of-type) .card-header:first-child { border-ra=
dius: 0px; }

.accordion > .card:not(:first-of-type):not(:last-of-type) { border-bottom: =
0px; border-radius: 0px; }

.accordion > .card:first-of-type { border-bottom: 0px; border-bottom-right-=
radius: 0px; border-bottom-left-radius: 0px; }

.accordion > .card:last-of-type { border-top-left-radius: 0px; border-top-r=
ight-radius: 0px; }

.accordion > .card .card-header { margin-bottom: -1px; }

.breadcrumb { display: flex; flex-wrap: wrap; padding: 0.75rem 1rem; margin=
-bottom: 1rem; list-style: none; background-color: rgb(233, 236, 239); bord=
er-radius: 0.25rem; }

.breadcrumb-item + .breadcrumb-item { padding-left: 0.5rem; }

.breadcrumb-item + .breadcrumb-item::before { display: inline-block; paddin=
g-right: 0.5rem; color: rgb(108, 117, 125); content: "/"; }

.breadcrumb-item + .breadcrumb-item:hover::before { text-decoration: underl=
ine; }

.breadcrumb-item + .breadcrumb-item:hover::before { text-decoration: none; =
}

.breadcrumb-item.active { color: rgb(108, 117, 125); }

.pagination { display: flex; padding-left: 0px; list-style: none; border-ra=
dius: 0.25rem; }

.page-link { position: relative; display: block; padding: 0.5rem 0.75rem; m=
argin-left: -1px; line-height: 1.25; color: rgb(0, 123, 255); background-co=
lor: rgb(255, 255, 255); border: 1px solid rgb(222, 226, 230); }

.page-link:hover { z-index: 2; color: rgb(0, 86, 179); text-decoration: non=
e; background-color: rgb(233, 236, 239); border-color: rgb(222, 226, 230); =
}

.page-link:focus { z-index: 2; outline: 0px; box-shadow: rgba(0, 123, 255, =
0.25) 0px 0px 0px 0.2rem; }

.page-item:first-child .page-link { margin-left: 0px; border-top-left-radiu=
s: 0.25rem; border-bottom-left-radius: 0.25rem; }

.page-item:last-child .page-link { border-top-right-radius: 0.25rem; border=
-bottom-right-radius: 0.25rem; }

.page-item.active .page-link { z-index: 1; color: rgb(255, 255, 255); backg=
round-color: rgb(0, 123, 255); border-color: rgb(0, 123, 255); }

.page-item.disabled .page-link { color: rgb(108, 117, 125); pointer-events:=
 none; cursor: auto; background-color: rgb(255, 255, 255); border-color: rg=
b(222, 226, 230); }

.pagination-lg .page-link { padding: 0.75rem 1.5rem; font-size: 1.25rem; li=
ne-height: 1.5; }

.pagination-lg .page-item:first-child .page-link { border-top-left-radius: =
0.3rem; border-bottom-left-radius: 0.3rem; }

.pagination-lg .page-item:last-child .page-link { border-top-right-radius: =
0.3rem; border-bottom-right-radius: 0.3rem; }

.pagination-sm .page-link { padding: 0.25rem 0.5rem; font-size: 0.875rem; l=
ine-height: 1.5; }

.pagination-sm .page-item:first-child .page-link { border-top-left-radius: =
0.2rem; border-bottom-left-radius: 0.2rem; }

.pagination-sm .page-item:last-child .page-link { border-top-right-radius: =
0.2rem; border-bottom-right-radius: 0.2rem; }

.badge { display: inline-block; padding: 0.25em 0.4em; font-size: 75%; font=
-weight: 700; line-height: 1; text-align: center; white-space: nowrap; vert=
ical-align: baseline; border-radius: 0.25rem; transition: color 0.15s ease-=
in-out 0s, background-color 0.15s ease-in-out 0s, border-color 0.15s ease-i=
n-out 0s, box-shadow 0.15s ease-in-out 0s; }

@media (prefers-reduced-motion: reduce) {
  .badge { transition: none 0s ease 0s; }
}

a.badge:focus, a.badge:hover { text-decoration: none; }

.badge:empty { display: none; }

.btn .badge { position: relative; top: -1px; }

.badge-pill { padding-right: 0.6em; padding-left: 0.6em; border-radius: 10r=
em; }

.badge-primary { color: rgb(255, 255, 255); background-color: rgb(0, 123, 2=
55); }

a.badge-primary:focus, a.badge-primary:hover { color: rgb(255, 255, 255); b=
ackground-color: rgb(0, 98, 204); }

a.badge-primary.focus, a.badge-primary:focus { outline: 0px; box-shadow: rg=
ba(0, 123, 255, 0.5) 0px 0px 0px 0.2rem; }

.badge-secondary { color: rgb(255, 255, 255); background-color: rgb(108, 11=
7, 125); }

a.badge-secondary:focus, a.badge-secondary:hover { color: rgb(255, 255, 255=
); background-color: rgb(84, 91, 98); }

a.badge-secondary.focus, a.badge-secondary:focus { outline: 0px; box-shadow=
: rgba(108, 117, 125, 0.5) 0px 0px 0px 0.2rem; }

.badge-success { color: rgb(255, 255, 255); background-color: rgb(40, 167, =
69); }

a.badge-success:focus, a.badge-success:hover { color: rgb(255, 255, 255); b=
ackground-color: rgb(30, 126, 52); }

a.badge-success.focus, a.badge-success:focus { outline: 0px; box-shadow: rg=
ba(40, 167, 69, 0.5) 0px 0px 0px 0.2rem; }

.badge-info { color: rgb(255, 255, 255); background-color: rgb(23, 162, 184=
); }

a.badge-info:focus, a.badge-info:hover { color: rgb(255, 255, 255); backgro=
und-color: rgb(17, 122, 139); }

a.badge-info.focus, a.badge-info:focus { outline: 0px; box-shadow: rgba(23,=
 162, 184, 0.5) 0px 0px 0px 0.2rem; }

.badge-warning { color: rgb(33, 37, 41); background-color: rgb(255, 193, 7)=
; }

a.badge-warning:focus, a.badge-warning:hover { color: rgb(33, 37, 41); back=
ground-color: rgb(211, 158, 0); }

a.badge-warning.focus, a.badge-warning:focus { outline: 0px; box-shadow: rg=
ba(255, 193, 7, 0.5) 0px 0px 0px 0.2rem; }

.badge-danger { color: rgb(255, 255, 255); background-color: rgb(220, 53, 6=
9); }

a.badge-danger:focus, a.badge-danger:hover { color: rgb(255, 255, 255); bac=
kground-color: rgb(189, 33, 48); }

a.badge-danger.focus, a.badge-danger:focus { outline: 0px; box-shadow: rgba=
(220, 53, 69, 0.5) 0px 0px 0px 0.2rem; }

.badge-light { color: rgb(33, 37, 41); background-color: rgb(248, 249, 250)=
; }

a.badge-light:focus, a.badge-light:hover { color: rgb(33, 37, 41); backgrou=
nd-color: rgb(218, 224, 229); }

a.badge-light.focus, a.badge-light:focus { outline: 0px; box-shadow: rgba(2=
48, 249, 250, 0.5) 0px 0px 0px 0.2rem; }

.badge-dark { color: rgb(255, 255, 255); background-color: rgb(52, 58, 64);=
 }

a.badge-dark:focus, a.badge-dark:hover { color: rgb(255, 255, 255); backgro=
und-color: rgb(29, 33, 36); }

a.badge-dark.focus, a.badge-dark:focus { outline: 0px; box-shadow: rgba(52,=
 58, 64, 0.5) 0px 0px 0px 0.2rem; }

.jumbotron { padding: 2rem 1rem; margin-bottom: 2rem; background-color: rgb=
(233, 236, 239); border-radius: 0.3rem; }

@media (min-width: 576px) {
  .jumbotron { padding: 4rem 2rem; }
}

.jumbotron-fluid { padding-right: 0px; padding-left: 0px; border-radius: 0p=
x; }

.alert { position: relative; padding: 0.75rem 1.25rem; margin-bottom: 1rem;=
 border: 1px solid transparent; border-radius: 0.25rem; }

.alert-heading { color: inherit; }

.alert-link { font-weight: 700; }

.alert-dismissible { padding-right: 4rem; }

.alert-dismissible .close { position: absolute; top: 0px; right: 0px; paddi=
ng: 0.75rem 1.25rem; color: inherit; }

.alert-primary { color: rgb(0, 64, 133); background-color: rgb(204, 229, 25=
5); border-color: rgb(184, 218, 255); }

.alert-primary hr { border-top-color: rgb(159, 205, 255); }

.alert-primary .alert-link { color: rgb(0, 39, 82); }

.alert-secondary { color: rgb(56, 61, 65); background-color: rgb(226, 227, =
229); border-color: rgb(214, 216, 219); }

.alert-secondary hr { border-top-color: rgb(200, 203, 207); }

.alert-secondary .alert-link { color: rgb(32, 35, 38); }

.alert-success { color: rgb(21, 87, 36); background-color: rgb(212, 237, 21=
8); border-color: rgb(195, 230, 203); }

.alert-success hr { border-top-color: rgb(177, 223, 187); }

.alert-success .alert-link { color: rgb(11, 46, 19); }

.alert-info { color: rgb(12, 84, 96); background-color: rgb(209, 236, 241);=
 border-color: rgb(190, 229, 235); }

.alert-info hr { border-top-color: rgb(171, 221, 229); }

.alert-info .alert-link { color: rgb(6, 44, 51); }

.alert-warning { color: rgb(133, 100, 4); background-color: rgb(255, 243, 2=
05); border-color: rgb(255, 238, 186); }

.alert-warning hr { border-top-color: rgb(255, 232, 161); }

.alert-warning .alert-link { color: rgb(83, 63, 3); }

.alert-danger { color: rgb(114, 28, 36); background-color: rgb(248, 215, 21=
8); border-color: rgb(245, 198, 203); }

.alert-danger hr { border-top-color: rgb(241, 176, 183); }

.alert-danger .alert-link { color: rgb(73, 18, 23); }

.alert-light { color: rgb(129, 129, 130); background-color: rgb(254, 254, 2=
54); border-color: rgb(253, 253, 254); }

.alert-light hr { border-top-color: rgb(236, 236, 246); }

.alert-light .alert-link { color: rgb(104, 104, 104); }

.alert-dark { color: rgb(27, 30, 33); background-color: rgb(214, 216, 217);=
 border-color: rgb(198, 200, 202); }

.alert-dark hr { border-top-color: rgb(185, 187, 190); }

.alert-dark .alert-link { color: rgb(4, 5, 5); }

@-webkit-keyframes progress-bar-stripes {=20
  0% { background-position: 1rem 0px; }
  100% { background-position: 0px 0px; }
}

@keyframes progress-bar-stripes {=20
  0% { background-position: 1rem 0px; }
  100% { background-position: 0px 0px; }
}

.progress { display: flex; height: 1rem; overflow: hidden; font-size: 0.75r=
em; background-color: rgb(233, 236, 239); border-radius: 0.25rem; }

.progress-bar { display: flex; flex-direction: column; justify-content: cen=
ter; color: rgb(255, 255, 255); text-align: center; white-space: nowrap; ba=
ckground-color: rgb(0, 123, 255); transition: width 0.6s ease 0s; }

@media (prefers-reduced-motion: reduce) {
  .progress-bar { transition: none 0s ease 0s; }
}

.progress-bar-striped { background-image: linear-gradient(45deg, rgba(255, =
255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, =
0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent); ba=
ckground-size: 1rem 1rem; }

.progress-bar-animated { animation: 1s linear 0s infinite normal none runni=
ng progress-bar-stripes; }

@media (prefers-reduced-motion: reduce) {
  .progress-bar-animated { animation: 0s ease 0s 1 normal none running none=
; }
}

.media { display: flex; align-items: flex-start; }

.media-body { flex: 1 1 0%; }

.list-group { display: flex; flex-direction: column; padding-left: 0px; mar=
gin-bottom: 0px; }

.list-group-item-action { width: 100%; color: rgb(73, 80, 87); text-align: =
inherit; }

.list-group-item-action:focus, .list-group-item-action:hover { z-index: 1; =
color: rgb(73, 80, 87); text-decoration: none; background-color: rgb(248, 2=
49, 250); }

.list-group-item-action:active { color: rgb(33, 37, 41); background-color: =
rgb(233, 236, 239); }

.list-group-item { position: relative; display: block; padding: 0.75rem 1.2=
5rem; margin-bottom: -1px; background-color: rgb(255, 255, 255); border: 1p=
x solid rgba(0, 0, 0, 0.125); }

.list-group-item:first-child { border-top-left-radius: 0.25rem; border-top-=
right-radius: 0.25rem; }

.list-group-item:last-child { margin-bottom: 0px; border-bottom-right-radiu=
s: 0.25rem; border-bottom-left-radius: 0.25rem; }

.list-group-item.disabled, .list-group-item:disabled { color: rgb(108, 117,=
 125); pointer-events: none; background-color: rgb(255, 255, 255); }

.list-group-item.active { z-index: 2; color: rgb(255, 255, 255); background=
-color: rgb(0, 123, 255); border-color: rgb(0, 123, 255); }

.list-group-horizontal { flex-direction: row; }

.list-group-horizontal .list-group-item { margin-right: -1px; margin-bottom=
: 0px; }

.list-group-horizontal .list-group-item:first-child { border-top-left-radiu=
s: 0.25rem; border-bottom-left-radius: 0.25rem; border-top-right-radius: 0p=
x; }

.list-group-horizontal .list-group-item:last-child { margin-right: 0px; bor=
der-top-right-radius: 0.25rem; border-bottom-right-radius: 0.25rem; border-=
bottom-left-radius: 0px; }

@media (min-width: 576px) {
  .list-group-horizontal-sm { flex-direction: row; }
  .list-group-horizontal-sm .list-group-item { margin-right: -1px; margin-b=
ottom: 0px; }
  .list-group-horizontal-sm .list-group-item:first-child { border-top-left-=
radius: 0.25rem; border-bottom-left-radius: 0.25rem; border-top-right-radiu=
s: 0px; }
  .list-group-horizontal-sm .list-group-item:last-child { margin-right: 0px=
; border-top-right-radius: 0.25rem; border-bottom-right-radius: 0.25rem; bo=
rder-bottom-left-radius: 0px; }
}

@media (min-width: 768px) {
  .list-group-horizontal-md { flex-direction: row; }
  .list-group-horizontal-md .list-group-item { margin-right: -1px; margin-b=
ottom: 0px; }
  .list-group-horizontal-md .list-group-item:first-child { border-top-left-=
radius: 0.25rem; border-bottom-left-radius: 0.25rem; border-top-right-radiu=
s: 0px; }
  .list-group-horizontal-md .list-group-item:last-child { margin-right: 0px=
; border-top-right-radius: 0.25rem; border-bottom-right-radius: 0.25rem; bo=
rder-bottom-left-radius: 0px; }
}

@media (min-width: 992px) {
  .list-group-horizontal-lg { flex-direction: row; }
  .list-group-horizontal-lg .list-group-item { margin-right: -1px; margin-b=
ottom: 0px; }
  .list-group-horizontal-lg .list-group-item:first-child { border-top-left-=
radius: 0.25rem; border-bottom-left-radius: 0.25rem; border-top-right-radiu=
s: 0px; }
  .list-group-horizontal-lg .list-group-item:last-child { margin-right: 0px=
; border-top-right-radius: 0.25rem; border-bottom-right-radius: 0.25rem; bo=
rder-bottom-left-radius: 0px; }
}

@media (min-width: 1200px) {
  .list-group-horizontal-xl { flex-direction: row; }
  .list-group-horizontal-xl .list-group-item { margin-right: -1px; margin-b=
ottom: 0px; }
  .list-group-horizontal-xl .list-group-item:first-child { border-top-left-=
radius: 0.25rem; border-bottom-left-radius: 0.25rem; border-top-right-radiu=
s: 0px; }
  .list-group-horizontal-xl .list-group-item:last-child { margin-right: 0px=
; border-top-right-radius: 0.25rem; border-bottom-right-radius: 0.25rem; bo=
rder-bottom-left-radius: 0px; }
}

.list-group-flush .list-group-item { border-right: 0px; border-left: 0px; b=
order-radius: 0px; }

.list-group-flush .list-group-item:last-child { margin-bottom: -1px; }

.list-group-flush:first-child .list-group-item:first-child { border-top: 0p=
x; }

.list-group-flush:last-child .list-group-item:last-child { margin-bottom: 0=
px; border-bottom: 0px; }

.list-group-item-primary { color: rgb(0, 64, 133); background-color: rgb(18=
4, 218, 255); }

.list-group-item-primary.list-group-item-action:focus, .list-group-item-pri=
mary.list-group-item-action:hover { color: rgb(0, 64, 133); background-colo=
r: rgb(159, 205, 255); }

.list-group-item-primary.list-group-item-action.active { color: rgb(255, 25=
5, 255); background-color: rgb(0, 64, 133); border-color: rgb(0, 64, 133); =
}

.list-group-item-secondary { color: rgb(56, 61, 65); background-color: rgb(=
214, 216, 219); }

.list-group-item-secondary.list-group-item-action:focus, .list-group-item-s=
econdary.list-group-item-action:hover { color: rgb(56, 61, 65); background-=
color: rgb(200, 203, 207); }

.list-group-item-secondary.list-group-item-action.active { color: rgb(255, =
255, 255); background-color: rgb(56, 61, 65); border-color: rgb(56, 61, 65)=
; }

.list-group-item-success { color: rgb(21, 87, 36); background-color: rgb(19=
5, 230, 203); }

.list-group-item-success.list-group-item-action:focus, .list-group-item-suc=
cess.list-group-item-action:hover { color: rgb(21, 87, 36); background-colo=
r: rgb(177, 223, 187); }

.list-group-item-success.list-group-item-action.active { color: rgb(255, 25=
5, 255); background-color: rgb(21, 87, 36); border-color: rgb(21, 87, 36); =
}

.list-group-item-info { color: rgb(12, 84, 96); background-color: rgb(190, =
229, 235); }

.list-group-item-info.list-group-item-action:focus, .list-group-item-info.l=
ist-group-item-action:hover { color: rgb(12, 84, 96); background-color: rgb=
(171, 221, 229); }

.list-group-item-info.list-group-item-action.active { color: rgb(255, 255, =
255); background-color: rgb(12, 84, 96); border-color: rgb(12, 84, 96); }

.list-group-item-warning { color: rgb(133, 100, 4); background-color: rgb(2=
55, 238, 186); }

.list-group-item-warning.list-group-item-action:focus, .list-group-item-war=
ning.list-group-item-action:hover { color: rgb(133, 100, 4); background-col=
or: rgb(255, 232, 161); }

.list-group-item-warning.list-group-item-action.active { color: rgb(255, 25=
5, 255); background-color: rgb(133, 100, 4); border-color: rgb(133, 100, 4)=
; }

.list-group-item-danger { color: rgb(114, 28, 36); background-color: rgb(24=
5, 198, 203); }

.list-group-item-danger.list-group-item-action:focus, .list-group-item-dang=
er.list-group-item-action:hover { color: rgb(114, 28, 36); background-color=
: rgb(241, 176, 183); }

.list-group-item-danger.list-group-item-action.active { color: rgb(255, 255=
, 255); background-color: rgb(114, 28, 36); border-color: rgb(114, 28, 36);=
 }

.list-group-item-light { color: rgb(129, 129, 130); background-color: rgb(2=
53, 253, 254); }

.list-group-item-light.list-group-item-action:focus, .list-group-item-light=
.list-group-item-action:hover { color: rgb(129, 129, 130); background-color=
: rgb(236, 236, 246); }

.list-group-item-light.list-group-item-action.active { color: rgb(255, 255,=
 255); background-color: rgb(129, 129, 130); border-color: rgb(129, 129, 13=
0); }

.list-group-item-dark { color: rgb(27, 30, 33); background-color: rgb(198, =
200, 202); }

.list-group-item-dark.list-group-item-action:focus, .list-group-item-dark.l=
ist-group-item-action:hover { color: rgb(27, 30, 33); background-color: rgb=
(185, 187, 190); }

.list-group-item-dark.list-group-item-action.active { color: rgb(255, 255, =
255); background-color: rgb(27, 30, 33); border-color: rgb(27, 30, 33); }

.close { float: right; font-size: 1.5rem; font-weight: 700; line-height: 1;=
 color: rgb(0, 0, 0); text-shadow: rgb(255, 255, 255) 0px 1px 0px; opacity:=
 0.5; }

.close:hover { color: rgb(0, 0, 0); text-decoration: none; }

.close:not(:disabled):not(.disabled):focus, .close:not(:disabled):not(.disa=
bled):hover { opacity: 0.75; }

button.close { padding: 0px; background-color: transparent; border: 0px; ap=
pearance: none; }

a.close.disabled { pointer-events: none; }

.toast { max-width: 350px; overflow: hidden; font-size: 0.875rem; backgroun=
d-color: rgba(255, 255, 255, 0.85); background-clip: padding-box; border: 1=
px solid rgba(0, 0, 0, 0.1); box-shadow: rgba(0, 0, 0, 0.1) 0px 0.25rem 0.7=
5rem; backdrop-filter: blur(10px); opacity: 0; border-radius: 0.25rem; }

.toast:not(:last-child) { margin-bottom: 0.75rem; }

.toast.showing { opacity: 1; }

.toast.show { display: block; opacity: 1; }

.toast.hide { display: none; }

.toast-header { display: flex; align-items: center; padding: 0.25rem 0.75re=
m; color: rgb(108, 117, 125); background-color: rgba(255, 255, 255, 0.85); =
background-clip: padding-box; border-bottom: 1px solid rgba(0, 0, 0, 0.05);=
 }

.toast-body { padding: 0.75rem; }

.modal-open { overflow: hidden; }

.modal-open .modal { overflow: hidden auto; }

.modal { position: fixed; top: 0px; left: 0px; z-index: 1050; display: none=
; width: 100%; height: 100%; overflow: hidden; outline: 0px; }

.modal-dialog { position: relative; width: auto; margin: 0.5rem; pointer-ev=
ents: none; }

.modal.fade .modal-dialog { transition: transform 0.3s ease-out 0s, -webkit=
-transform 0.3s ease-out 0s; transform: translate(0px, -50px); }

@media (prefers-reduced-motion: reduce) {
  .modal.fade .modal-dialog { transition: none 0s ease 0s; }
}

.modal.show .modal-dialog { transform: none; }

.modal-dialog-scrollable { display: flex; max-height: calc(100% - 1rem); }

.modal-dialog-scrollable .modal-content { max-height: calc(100vh - 1rem); o=
verflow: hidden; }

.modal-dialog-scrollable .modal-footer, .modal-dialog-scrollable .modal-hea=
der { flex-shrink: 0; }

.modal-dialog-scrollable .modal-body { overflow-y: auto; }

.modal-dialog-centered { display: flex; align-items: center; min-height: ca=
lc(100% - 1rem); }

.modal-dialog-centered::before { display: block; height: calc(100vh - 1rem)=
; content: ""; }

.modal-dialog-centered.modal-dialog-scrollable { flex-direction: column; ju=
stify-content: center; height: 100%; }

.modal-dialog-centered.modal-dialog-scrollable .modal-content { max-height:=
 none; }

.modal-dialog-centered.modal-dialog-scrollable::before { content: none; }

.modal-content { position: relative; display: flex; flex-direction: column;=
 width: 100%; pointer-events: auto; background-color: rgb(255, 255, 255); b=
ackground-clip: padding-box; border: 1px solid rgba(0, 0, 0, 0.2); border-r=
adius: 0.3rem; outline: 0px; }

.modal-backdrop { position: fixed; top: 0px; left: 0px; z-index: 1040; widt=
h: 100vw; height: 100vh; background-color: rgb(0, 0, 0); }

.modal-backdrop.fade { opacity: 0; }

.modal-backdrop.show { opacity: 0.5; }

.modal-header { display: flex; align-items: flex-start; justify-content: sp=
ace-between; padding: 1rem; border-bottom: 1px solid rgb(222, 226, 230); bo=
rder-top-left-radius: 0.3rem; border-top-right-radius: 0.3rem; }

.modal-header .close { padding: 1rem; margin: -1rem -1rem -1rem auto; }

.modal-title { margin-bottom: 0px; line-height: 1.5; }

.modal-body { position: relative; flex: 1 1 auto; padding: 1rem; }

.modal-footer { display: flex; align-items: center; justify-content: flex-e=
nd; padding: 1rem; border-top: 1px solid rgb(222, 226, 230); border-bottom-=
right-radius: 0.3rem; border-bottom-left-radius: 0.3rem; }

.modal-footer > :not(:first-child) { margin-left: 0.25rem; }

.modal-footer > :not(:last-child) { margin-right: 0.25rem; }

.modal-scrollbar-measure { position: absolute; top: -9999px; width: 50px; h=
eight: 50px; overflow: scroll; }

@media (min-width: 576px) {
  .modal-dialog { max-width: 500px; margin: 1.75rem auto; }
  .modal-dialog-scrollable { max-height: calc(100% - 3.5rem); }
  .modal-dialog-scrollable .modal-content { max-height: calc(100vh - 3.5rem=
); }
  .modal-dialog-centered { min-height: calc(100% - 3.5rem); }
  .modal-dialog-centered::before { height: calc(100vh - 3.5rem); }
  .modal-sm { max-width: 300px; }
}

@media (min-width: 992px) {
  .modal-lg, .modal-xl { max-width: 800px; }
}

@media (min-width: 1200px) {
  .modal-xl { max-width: 1140px; }
}

.tooltip { position: absolute; z-index: 1070; display: block; margin: 0px; =
font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvet=
ica Neue", Arial, "Noto Sans", sans-serif, "Apple Color Emoji", "Segoe UI E=
moji", "Segoe UI Symbol", "Noto Color Emoji"; font-style: normal; font-weig=
ht: 400; line-height: 1.5; text-align: start; text-decoration: none; text-s=
hadow: none; text-transform: none; letter-spacing: normal; word-break: norm=
al; word-spacing: normal; white-space: normal; line-break: auto; font-size:=
 0.875rem; overflow-wrap: break-word; opacity: 0; }

.tooltip.show { opacity: 0.9; }

.tooltip .arrow { position: absolute; display: block; width: 0.8rem; height=
: 0.4rem; }

.tooltip .arrow::before { position: absolute; content: ""; border-color: tr=
ansparent; border-style: solid; }

.bs-tooltip-auto[x-placement^=3D"top"], .bs-tooltip-top { padding: 0.4rem 0=
px; }

.bs-tooltip-auto[x-placement^=3D"top"] .arrow, .bs-tooltip-top .arrow { bot=
tom: 0px; }

.bs-tooltip-auto[x-placement^=3D"top"] .arrow::before, .bs-tooltip-top .arr=
ow::before { top: 0px; border-width: 0.4rem 0.4rem 0px; border-top-color: r=
gb(0, 0, 0); }

.bs-tooltip-auto[x-placement^=3D"right"], .bs-tooltip-right { padding: 0px =
0.4rem; }

.bs-tooltip-auto[x-placement^=3D"right"] .arrow, .bs-tooltip-right .arrow {=
 left: 0px; width: 0.4rem; height: 0.8rem; }

.bs-tooltip-auto[x-placement^=3D"right"] .arrow::before, .bs-tooltip-right =
.arrow::before { right: 0px; border-width: 0.4rem 0.4rem 0.4rem 0px; border=
-right-color: rgb(0, 0, 0); }

.bs-tooltip-auto[x-placement^=3D"bottom"], .bs-tooltip-bottom { padding: 0.=
4rem 0px; }

.bs-tooltip-auto[x-placement^=3D"bottom"] .arrow, .bs-tooltip-bottom .arrow=
 { top: 0px; }

.bs-tooltip-auto[x-placement^=3D"bottom"] .arrow::before, .bs-tooltip-botto=
m .arrow::before { bottom: 0px; border-width: 0px 0.4rem 0.4rem; border-bot=
tom-color: rgb(0, 0, 0); }

.bs-tooltip-auto[x-placement^=3D"left"], .bs-tooltip-left { padding: 0px 0.=
4rem; }

.bs-tooltip-auto[x-placement^=3D"left"] .arrow, .bs-tooltip-left .arrow { r=
ight: 0px; width: 0.4rem; height: 0.8rem; }

.bs-tooltip-auto[x-placement^=3D"left"] .arrow::before, .bs-tooltip-left .a=
rrow::before { left: 0px; border-width: 0.4rem 0px 0.4rem 0.4rem; border-le=
ft-color: rgb(0, 0, 0); }

.tooltip-inner { max-width: 200px; padding: 0.25rem 0.5rem; color: rgb(255,=
 255, 255); text-align: center; background-color: rgb(0, 0, 0); border-radi=
us: 0.25rem; }

.popover { position: absolute; top: 0px; left: 0px; z-index: 1060; display:=
 block; max-width: 276px; font-family: -apple-system, BlinkMacSystemFont, "=
Segoe UI", Roboto, "Helvetica Neue", Arial, "Noto Sans", sans-serif, "Apple=
 Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji"; fon=
t-style: normal; font-weight: 400; line-height: 1.5; text-align: start; tex=
t-decoration: none; text-shadow: none; text-transform: none; letter-spacing=
: normal; word-break: normal; word-spacing: normal; white-space: normal; li=
ne-break: auto; font-size: 0.875rem; overflow-wrap: break-word; background-=
color: rgb(255, 255, 255); background-clip: padding-box; border: 1px solid =
rgba(0, 0, 0, 0.2); border-radius: 0.3rem; }

.popover .arrow { position: absolute; display: block; width: 1rem; height: =
0.5rem; margin: 0px 0.3rem; }

.popover .arrow::after, .popover .arrow::before { position: absolute; displ=
ay: block; content: ""; border-color: transparent; border-style: solid; }

.bs-popover-auto[x-placement^=3D"top"], .bs-popover-top { margin-bottom: 0.=
5rem; }

.bs-popover-auto[x-placement^=3D"top"] > .arrow, .bs-popover-top > .arrow {=
 bottom: calc((0.5rem + 1px) * -1); }

.bs-popover-auto[x-placement^=3D"top"] > .arrow::before, .bs-popover-top > =
.arrow::before { bottom: 0px; border-width: 0.5rem 0.5rem 0px; border-top-c=
olor: rgba(0, 0, 0, 0.25); }

.bs-popover-auto[x-placement^=3D"top"] > .arrow::after, .bs-popover-top > .=
arrow::after { bottom: 1px; border-width: 0.5rem 0.5rem 0px; border-top-col=
or: rgb(255, 255, 255); }

.bs-popover-auto[x-placement^=3D"right"], .bs-popover-right { margin-left: =
0.5rem; }

.bs-popover-auto[x-placement^=3D"right"] > .arrow, .bs-popover-right > .arr=
ow { left: calc((0.5rem + 1px) * -1); width: 0.5rem; height: 1rem; margin: =
0.3rem 0px; }

.bs-popover-auto[x-placement^=3D"right"] > .arrow::before, .bs-popover-righ=
t > .arrow::before { left: 0px; border-width: 0.5rem 0.5rem 0.5rem 0px; bor=
der-right-color: rgba(0, 0, 0, 0.25); }

.bs-popover-auto[x-placement^=3D"right"] > .arrow::after, .bs-popover-right=
 > .arrow::after { left: 1px; border-width: 0.5rem 0.5rem 0.5rem 0px; borde=
r-right-color: rgb(255, 255, 255); }

.bs-popover-auto[x-placement^=3D"bottom"], .bs-popover-bottom { margin-top:=
 0.5rem; }

.bs-popover-auto[x-placement^=3D"bottom"] > .arrow, .bs-popover-bottom > .a=
rrow { top: calc((0.5rem + 1px) * -1); }

.bs-popover-auto[x-placement^=3D"bottom"] > .arrow::before, .bs-popover-bot=
tom > .arrow::before { top: 0px; border-width: 0px 0.5rem 0.5rem; border-bo=
ttom-color: rgba(0, 0, 0, 0.25); }

.bs-popover-auto[x-placement^=3D"bottom"] > .arrow::after, .bs-popover-bott=
om > .arrow::after { top: 1px; border-width: 0px 0.5rem 0.5rem; border-bott=
om-color: rgb(255, 255, 255); }

.bs-popover-auto[x-placement^=3D"bottom"] .popover-header::before, .bs-popo=
ver-bottom .popover-header::before { position: absolute; top: 0px; left: 50=
%; display: block; width: 1rem; margin-left: -0.5rem; content: ""; border-b=
ottom: 1px solid rgb(247, 247, 247); }

.bs-popover-auto[x-placement^=3D"left"], .bs-popover-left { margin-right: 0=
.5rem; }

.bs-popover-auto[x-placement^=3D"left"] > .arrow, .bs-popover-left > .arrow=
 { right: calc((0.5rem + 1px) * -1); width: 0.5rem; height: 1rem; margin: 0=
.3rem 0px; }

.bs-popover-auto[x-placement^=3D"left"] > .arrow::before, .bs-popover-left =
> .arrow::before { right: 0px; border-width: 0.5rem 0px 0.5rem 0.5rem; bord=
er-left-color: rgba(0, 0, 0, 0.25); }

.bs-popover-auto[x-placement^=3D"left"] > .arrow::after, .bs-popover-left >=
 .arrow::after { right: 1px; border-width: 0.5rem 0px 0.5rem 0.5rem; border=
-left-color: rgb(255, 255, 255); }

.popover-header { padding: 0.5rem 0.75rem; margin-bottom: 0px; font-size: 1=
rem; background-color: rgb(247, 247, 247); border-bottom: 1px solid rgb(235=
, 235, 235); border-top-left-radius: calc(0.3rem - 1px); border-top-right-r=
adius: calc(0.3rem - 1px); }

.popover-header:empty { display: none; }

.popover-body { padding: 0.5rem 0.75rem; color: rgb(33, 37, 41); }

.carousel { position: relative; }

.carousel.pointer-event { touch-action: pan-y; }

.carousel-inner { position: relative; width: 100%; overflow: hidden; }

.carousel-inner::after { display: block; clear: both; content: ""; }

.carousel-item { position: relative; display: none; float: left; width: 100=
%; margin-right: -100%; backface-visibility: hidden; transition: transform =
0.6s ease-in-out 0s, -webkit-transform 0.6s ease-in-out 0s; }

@media (prefers-reduced-motion: reduce) {
  .carousel-item { transition: none 0s ease 0s; }
}

.carousel-item-next, .carousel-item-prev, .carousel-item.active { display: =
block; }

.active.carousel-item-right, .carousel-item-next:not(.carousel-item-left) {=
 transform: translateX(100%); }

.active.carousel-item-left, .carousel-item-prev:not(.carousel-item-right) {=
 transform: translateX(-100%); }

.carousel-fade .carousel-item { opacity: 0; transition-property: opacity; t=
ransform: none; }

.carousel-fade .carousel-item-next.carousel-item-left, .carousel-fade .caro=
usel-item-prev.carousel-item-right, .carousel-fade .carousel-item.active { =
z-index: 1; opacity: 1; }

.carousel-fade .active.carousel-item-left, .carousel-fade .active.carousel-=
item-right { z-index: 0; opacity: 0; transition: opacity 0s ease 0.6s; }

@media (prefers-reduced-motion: reduce) {
  .carousel-fade .active.carousel-item-left, .carousel-fade .active.carouse=
l-item-right { transition: none 0s ease 0s; }
}

.carousel-control-next, .carousel-control-prev { position: absolute; top: 0=
px; bottom: 0px; z-index: 1; display: flex; align-items: center; justify-co=
ntent: center; width: 15%; color: rgb(255, 255, 255); text-align: center; o=
pacity: 0.5; transition: opacity 0.15s ease 0s; }

@media (prefers-reduced-motion: reduce) {
  .carousel-control-next, .carousel-control-prev { transition: none 0s ease=
 0s; }
}

.carousel-control-next:focus, .carousel-control-next:hover, .carousel-contr=
ol-prev:focus, .carousel-control-prev:hover { color: rgb(255, 255, 255); te=
xt-decoration: none; outline: 0px; opacity: 0.9; }

.carousel-control-prev { left: 0px; }

.carousel-control-next { right: 0px; }

.carousel-control-next-icon, .carousel-control-prev-icon { display: inline-=
block; width: 20px; height: 20px; background: 50% center / 100% 100% no-rep=
eat; }

.carousel-control-prev-icon { background-image: url("data:image/svg+xml,%3c=
svg xmlns=3D'http://www.w3.org/2000/svg' fill=3D'%23fff' viewBox=3D'0 0 8 8=
'%3e%3cpath d=3D'M5.25 0l-4 4 4 4 1.5-1.5-2.5-2.5 2.5-2.5-1.5-1.5z'/%3e%3c/=
svg%3e"); }

.carousel-control-next-icon { background-image: url("data:image/svg+xml,%3c=
svg xmlns=3D'http://www.w3.org/2000/svg' fill=3D'%23fff' viewBox=3D'0 0 8 8=
'%3e%3cpath d=3D'M2.75 0l-1.5 1.5 2.5 2.5-2.5 2.5 1.5 1.5 4-4-4-4z'/%3e%3c/=
svg%3e"); }

.carousel-indicators { position: absolute; right: 0px; bottom: 0px; left: 0=
px; z-index: 15; display: flex; justify-content: center; padding-left: 0px;=
 margin-right: 15%; margin-left: 15%; list-style: none; }

.carousel-indicators li { box-sizing: content-box; flex: 0 1 auto; width: 3=
0px; height: 3px; margin-right: 3px; margin-left: 3px; text-indent: -999px;=
 cursor: pointer; background-color: rgb(255, 255, 255); background-clip: pa=
dding-box; border-top: 10px solid transparent; border-bottom: 10px solid tr=
ansparent; opacity: 0.5; transition: opacity 0.6s ease 0s; }

@media (prefers-reduced-motion: reduce) {
  .carousel-indicators li { transition: none 0s ease 0s; }
}

.carousel-indicators .active { opacity: 1; }

.carousel-caption { position: absolute; right: 15%; bottom: 20px; left: 15%=
; z-index: 10; padding-top: 20px; padding-bottom: 20px; color: rgb(255, 255=
, 255); text-align: center; }

@-webkit-keyframes spinner-border {=20
  100% { transform: rotate(360deg); }
}

@keyframes spinner-border {=20
  100% { transform: rotate(360deg); }
}

.spinner-border { display: inline-block; width: 2rem; height: 2rem; vertica=
l-align: text-bottom; border-width: 0.25em; border-style: solid; border-col=
or: currentcolor transparent currentcolor currentcolor; border-image: initi=
al; border-radius: 50%; animation: 0.75s linear 0s infinite normal none run=
ning spinner-border; }

.spinner-border-sm { width: 1rem; height: 1rem; border-width: 0.2em; }

@-webkit-keyframes spinner-grow {=20
  0% { transform: scale(0); }
  50% { opacity: 1; }
}

@keyframes spinner-grow {=20
  0% { transform: scale(0); }
  50% { opacity: 1; }
}

.spinner-grow { display: inline-block; width: 2rem; height: 2rem; vertical-=
align: text-bottom; background-color: currentcolor; border-radius: 50%; opa=
city: 0; animation: 0.75s linear 0s infinite normal none running spinner-gr=
ow; }

.spinner-grow-sm { width: 1rem; height: 1rem; }

.align-baseline { vertical-align: baseline !important; }

.align-top { vertical-align: top !important; }

.align-middle { vertical-align: middle !important; }

.align-bottom { vertical-align: bottom !important; }

.align-text-bottom { vertical-align: text-bottom !important; }

.align-text-top { vertical-align: text-top !important; }

.bg-primary { background-color: rgb(0, 123, 255) !important; }

a.bg-primary:focus, a.bg-primary:hover, button.bg-primary:focus, button.bg-=
primary:hover { background-color: rgb(0, 98, 204) !important; }

.bg-secondary { background-color: rgb(108, 117, 125) !important; }

a.bg-secondary:focus, a.bg-secondary:hover, button.bg-secondary:focus, butt=
on.bg-secondary:hover { background-color: rgb(84, 91, 98) !important; }

.bg-success { background-color: rgb(40, 167, 69) !important; }

a.bg-success:focus, a.bg-success:hover, button.bg-success:focus, button.bg-=
success:hover { background-color: rgb(30, 126, 52) !important; }

.bg-info { background-color: rgb(23, 162, 184) !important; }

a.bg-info:focus, a.bg-info:hover, button.bg-info:focus, button.bg-info:hove=
r { background-color: rgb(17, 122, 139) !important; }

.bg-warning { background-color: rgb(255, 193, 7) !important; }

a.bg-warning:focus, a.bg-warning:hover, button.bg-warning:focus, button.bg-=
warning:hover { background-color: rgb(211, 158, 0) !important; }

.bg-danger { background-color: rgb(220, 53, 69) !important; }

a.bg-danger:focus, a.bg-danger:hover, button.bg-danger:focus, button.bg-dan=
ger:hover { background-color: rgb(189, 33, 48) !important; }

.bg-light { background-color: rgb(248, 249, 250) !important; }

a.bg-light:focus, a.bg-light:hover, button.bg-light:focus, button.bg-light:=
hover { background-color: rgb(218, 224, 229) !important; }

.bg-dark { background-color: rgb(52, 58, 64) !important; }

a.bg-dark:focus, a.bg-dark:hover, button.bg-dark:focus, button.bg-dark:hove=
r { background-color: rgb(29, 33, 36) !important; }

.bg-white { background-color: rgb(255, 255, 255) !important; }

.bg-transparent { background-color: transparent !important; }

.border { border: 1px solid rgb(222, 226, 230) !important; }

.border-top { border-top: 1px solid rgb(222, 226, 230) !important; }

.border-right { border-right: 1px solid rgb(222, 226, 230) !important; }

.border-bottom { border-bottom: 1px solid rgb(222, 226, 230) !important; }

.border-left { border-left: 1px solid rgb(222, 226, 230) !important; }

.border-0 { border: 0px !important; }

.border-top-0 { border-top: 0px !important; }

.border-right-0 { border-right: 0px !important; }

.border-bottom-0 { border-bottom: 0px !important; }

.border-left-0 { border-left: 0px !important; }

.border-primary { border-color: rgb(0, 123, 255) !important; }

.border-secondary { border-color: rgb(108, 117, 125) !important; }

.border-success { border-color: rgb(40, 167, 69) !important; }

.border-info { border-color: rgb(23, 162, 184) !important; }

.border-warning { border-color: rgb(255, 193, 7) !important; }

.border-danger { border-color: rgb(220, 53, 69) !important; }

.border-light { border-color: rgb(248, 249, 250) !important; }

.border-dark { border-color: rgb(52, 58, 64) !important; }

.border-white { border-color: rgb(255, 255, 255) !important; }

.rounded-sm { border-radius: 0.2rem !important; }

.rounded { border-radius: 0.25rem !important; }

.rounded-top { border-top-left-radius: 0.25rem !important; border-top-right=
-radius: 0.25rem !important; }

.rounded-right { border-top-right-radius: 0.25rem !important; border-bottom=
-right-radius: 0.25rem !important; }

.rounded-bottom { border-bottom-right-radius: 0.25rem !important; border-bo=
ttom-left-radius: 0.25rem !important; }

.rounded-left { border-top-left-radius: 0.25rem !important; border-bottom-l=
eft-radius: 0.25rem !important; }

.rounded-lg { border-radius: 0.3rem !important; }

.rounded-circle { border-radius: 50% !important; }

.rounded-pill { border-radius: 50rem !important; }

.rounded-0 { border-radius: 0px !important; }

.clearfix::after { display: block; clear: both; content: ""; }

.d-none { display: none !important; }

.d-inline { display: inline !important; }

.d-inline-block { display: inline-block !important; }

.d-block { display: block !important; }

.d-table { display: table !important; }

.d-table-row { display: table-row !important; }

.d-table-cell { display: table-cell !important; }

.d-flex { display: flex !important; }

.d-inline-flex { display: inline-flex !important; }

@media (min-width: 576px) {
  .d-sm-none { display: none !important; }
  .d-sm-inline { display: inline !important; }
  .d-sm-inline-block { display: inline-block !important; }
  .d-sm-block { display: block !important; }
  .d-sm-table { display: table !important; }
  .d-sm-table-row { display: table-row !important; }
  .d-sm-table-cell { display: table-cell !important; }
  .d-sm-flex { display: flex !important; }
  .d-sm-inline-flex { display: inline-flex !important; }
}

@media (min-width: 768px) {
  .d-md-none { display: none !important; }
  .d-md-inline { display: inline !important; }
  .d-md-inline-block { display: inline-block !important; }
  .d-md-block { display: block !important; }
  .d-md-table { display: table !important; }
  .d-md-table-row { display: table-row !important; }
  .d-md-table-cell { display: table-cell !important; }
  .d-md-flex { display: flex !important; }
  .d-md-inline-flex { display: inline-flex !important; }
}

@media (min-width: 992px) {
  .d-lg-none { display: none !important; }
  .d-lg-inline { display: inline !important; }
  .d-lg-inline-block { display: inline-block !important; }
  .d-lg-block { display: block !important; }
  .d-lg-table { display: table !important; }
  .d-lg-table-row { display: table-row !important; }
  .d-lg-table-cell { display: table-cell !important; }
  .d-lg-flex { display: flex !important; }
  .d-lg-inline-flex { display: inline-flex !important; }
}

@media (min-width: 1200px) {
  .d-xl-none { display: none !important; }
  .d-xl-inline { display: inline !important; }
  .d-xl-inline-block { display: inline-block !important; }
  .d-xl-block { display: block !important; }
  .d-xl-table { display: table !important; }
  .d-xl-table-row { display: table-row !important; }
  .d-xl-table-cell { display: table-cell !important; }
  .d-xl-flex { display: flex !important; }
  .d-xl-inline-flex { display: inline-flex !important; }
}

@media print {
  .d-print-none { display: none !important; }
  .d-print-inline { display: inline !important; }
  .d-print-inline-block { display: inline-block !important; }
  .d-print-block { display: block !important; }
  .d-print-table { display: table !important; }
  .d-print-table-row { display: table-row !important; }
  .d-print-table-cell { display: table-cell !important; }
  .d-print-flex { display: flex !important; }
  .d-print-inline-flex { display: inline-flex !important; }
}

.embed-responsive { position: relative; display: block; width: 100%; paddin=
g: 0px; overflow: hidden; }

.embed-responsive::before { display: block; content: ""; }

.embed-responsive .embed-responsive-item, .embed-responsive embed, .embed-r=
esponsive iframe, .embed-responsive object, .embed-responsive video { posit=
ion: absolute; top: 0px; bottom: 0px; left: 0px; width: 100%; height: 100%;=
 border: 0px; }

.embed-responsive-21by9::before { padding-top: 42.8571%; }

.embed-responsive-16by9::before { padding-top: 56.25%; }

.embed-responsive-4by3::before { padding-top: 75%; }

.embed-responsive-1by1::before { padding-top: 100%; }

.flex-row { flex-direction: row !important; }

.flex-column { flex-direction: column !important; }

.flex-row-reverse { flex-direction: row-reverse !important; }

.flex-column-reverse { flex-direction: column-reverse !important; }

.flex-wrap { flex-wrap: wrap !important; }

.flex-nowrap { flex-wrap: nowrap !important; }

.flex-wrap-reverse { flex-wrap: wrap-reverse !important; }

.flex-fill { flex: 1 1 auto !important; }

.flex-grow-0 { flex-grow: 0 !important; }

.flex-grow-1 { flex-grow: 1 !important; }

.flex-shrink-0 { flex-shrink: 0 !important; }

.flex-shrink-1 { flex-shrink: 1 !important; }

.justify-content-start { justify-content: flex-start !important; }

.justify-content-end { justify-content: flex-end !important; }

.justify-content-center { justify-content: center !important; }

.justify-content-between { justify-content: space-between !important; }

.justify-content-around { justify-content: space-around !important; }

.align-items-start { align-items: flex-start !important; }

.align-items-end { align-items: flex-end !important; }

.align-items-center { align-items: center !important; }

.align-items-baseline { align-items: baseline !important; }

.align-items-stretch { align-items: stretch !important; }

.align-content-start { align-content: flex-start !important; }

.align-content-end { align-content: flex-end !important; }

.align-content-center { align-content: center !important; }

.align-content-between { align-content: space-between !important; }

.align-content-around { align-content: space-around !important; }

.align-content-stretch { align-content: stretch !important; }

.align-self-auto { align-self: auto !important; }

.align-self-start { align-self: flex-start !important; }

.align-self-end { align-self: flex-end !important; }

.align-self-center { align-self: center !important; }

.align-self-baseline { align-self: baseline !important; }

.align-self-stretch { align-self: stretch !important; }

@media (min-width: 576px) {
  .flex-sm-row { flex-direction: row !important; }
  .flex-sm-column { flex-direction: column !important; }
  .flex-sm-row-reverse { flex-direction: row-reverse !important; }
  .flex-sm-column-reverse { flex-direction: column-reverse !important; }
  .flex-sm-wrap { flex-wrap: wrap !important; }
  .flex-sm-nowrap { flex-wrap: nowrap !important; }
  .flex-sm-wrap-reverse { flex-wrap: wrap-reverse !important; }
  .flex-sm-fill { flex: 1 1 auto !important; }
  .flex-sm-grow-0 { flex-grow: 0 !important; }
  .flex-sm-grow-1 { flex-grow: 1 !important; }
  .flex-sm-shrink-0 { flex-shrink: 0 !important; }
  .flex-sm-shrink-1 { flex-shrink: 1 !important; }
  .justify-content-sm-start { justify-content: flex-start !important; }
  .justify-content-sm-end { justify-content: flex-end !important; }
  .justify-content-sm-center { justify-content: center !important; }
  .justify-content-sm-between { justify-content: space-between !important; =
}
  .justify-content-sm-around { justify-content: space-around !important; }
  .align-items-sm-start { align-items: flex-start !important; }
  .align-items-sm-end { align-items: flex-end !important; }
  .align-items-sm-center { align-items: center !important; }
  .align-items-sm-baseline { align-items: baseline !important; }
  .align-items-sm-stretch { align-items: stretch !important; }
  .align-content-sm-start { align-content: flex-start !important; }
  .align-content-sm-end { align-content: flex-end !important; }
  .align-content-sm-center { align-content: center !important; }
  .align-content-sm-between { align-content: space-between !important; }
  .align-content-sm-around { align-content: space-around !important; }
  .align-content-sm-stretch { align-content: stretch !important; }
  .align-self-sm-auto { align-self: auto !important; }
  .align-self-sm-start { align-self: flex-start !important; }
  .align-self-sm-end { align-self: flex-end !important; }
  .align-self-sm-center { align-self: center !important; }
  .align-self-sm-baseline { align-self: baseline !important; }
  .align-self-sm-stretch { align-self: stretch !important; }
}

@media (min-width: 768px) {
  .flex-md-row { flex-direction: row !important; }
  .flex-md-column { flex-direction: column !important; }
  .flex-md-row-reverse { flex-direction: row-reverse !important; }
  .flex-md-column-reverse { flex-direction: column-reverse !important; }
  .flex-md-wrap { flex-wrap: wrap !important; }
  .flex-md-nowrap { flex-wrap: nowrap !important; }
  .flex-md-wrap-reverse { flex-wrap: wrap-reverse !important; }
  .flex-md-fill { flex: 1 1 auto !important; }
  .flex-md-grow-0 { flex-grow: 0 !important; }
  .flex-md-grow-1 { flex-grow: 1 !important; }
  .flex-md-shrink-0 { flex-shrink: 0 !important; }
  .flex-md-shrink-1 { flex-shrink: 1 !important; }
  .justify-content-md-start { justify-content: flex-start !important; }
  .justify-content-md-end { justify-content: flex-end !important; }
  .justify-content-md-center { justify-content: center !important; }
  .justify-content-md-between { justify-content: space-between !important; =
}
  .justify-content-md-around { justify-content: space-around !important; }
  .align-items-md-start { align-items: flex-start !important; }
  .align-items-md-end { align-items: flex-end !important; }
  .align-items-md-center { align-items: center !important; }
  .align-items-md-baseline { align-items: baseline !important; }
  .align-items-md-stretch { align-items: stretch !important; }
  .align-content-md-start { align-content: flex-start !important; }
  .align-content-md-end { align-content: flex-end !important; }
  .align-content-md-center { align-content: center !important; }
  .align-content-md-between { align-content: space-between !important; }
  .align-content-md-around { align-content: space-around !important; }
  .align-content-md-stretch { align-content: stretch !important; }
  .align-self-md-auto { align-self: auto !important; }
  .align-self-md-start { align-self: flex-start !important; }
  .align-self-md-end { align-self: flex-end !important; }
  .align-self-md-center { align-self: center !important; }
  .align-self-md-baseline { align-self: baseline !important; }
  .align-self-md-stretch { align-self: stretch !important; }
}

@media (min-width: 992px) {
  .flex-lg-row { flex-direction: row !important; }
  .flex-lg-column { flex-direction: column !important; }
  .flex-lg-row-reverse { flex-direction: row-reverse !important; }
  .flex-lg-column-reverse { flex-direction: column-reverse !important; }
  .flex-lg-wrap { flex-wrap: wrap !important; }
  .flex-lg-nowrap { flex-wrap: nowrap !important; }
  .flex-lg-wrap-reverse { flex-wrap: wrap-reverse !important; }
  .flex-lg-fill { flex: 1 1 auto !important; }
  .flex-lg-grow-0 { flex-grow: 0 !important; }
  .flex-lg-grow-1 { flex-grow: 1 !important; }
  .flex-lg-shrink-0 { flex-shrink: 0 !important; }
  .flex-lg-shrink-1 { flex-shrink: 1 !important; }
  .justify-content-lg-start { justify-content: flex-start !important; }
  .justify-content-lg-end { justify-content: flex-end !important; }
  .justify-content-lg-center { justify-content: center !important; }
  .justify-content-lg-between { justify-content: space-between !important; =
}
  .justify-content-lg-around { justify-content: space-around !important; }
  .align-items-lg-start { align-items: flex-start !important; }
  .align-items-lg-end { align-items: flex-end !important; }
  .align-items-lg-center { align-items: center !important; }
  .align-items-lg-baseline { align-items: baseline !important; }
  .align-items-lg-stretch { align-items: stretch !important; }
  .align-content-lg-start { align-content: flex-start !important; }
  .align-content-lg-end { align-content: flex-end !important; }
  .align-content-lg-center { align-content: center !important; }
  .align-content-lg-between { align-content: space-between !important; }
  .align-content-lg-around { align-content: space-around !important; }
  .align-content-lg-stretch { align-content: stretch !important; }
  .align-self-lg-auto { align-self: auto !important; }
  .align-self-lg-start { align-self: flex-start !important; }
  .align-self-lg-end { align-self: flex-end !important; }
  .align-self-lg-center { align-self: center !important; }
  .align-self-lg-baseline { align-self: baseline !important; }
  .align-self-lg-stretch { align-self: stretch !important; }
}

@media (min-width: 1200px) {
  .flex-xl-row { flex-direction: row !important; }
  .flex-xl-column { flex-direction: column !important; }
  .flex-xl-row-reverse { flex-direction: row-reverse !important; }
  .flex-xl-column-reverse { flex-direction: column-reverse !important; }
  .flex-xl-wrap { flex-wrap: wrap !important; }
  .flex-xl-nowrap { flex-wrap: nowrap !important; }
  .flex-xl-wrap-reverse { flex-wrap: wrap-reverse !important; }
  .flex-xl-fill { flex: 1 1 auto !important; }
  .flex-xl-grow-0 { flex-grow: 0 !important; }
  .flex-xl-grow-1 { flex-grow: 1 !important; }
  .flex-xl-shrink-0 { flex-shrink: 0 !important; }
  .flex-xl-shrink-1 { flex-shrink: 1 !important; }
  .justify-content-xl-start { justify-content: flex-start !important; }
  .justify-content-xl-end { justify-content: flex-end !important; }
  .justify-content-xl-center { justify-content: center !important; }
  .justify-content-xl-between { justify-content: space-between !important; =
}
  .justify-content-xl-around { justify-content: space-around !important; }
  .align-items-xl-start { align-items: flex-start !important; }
  .align-items-xl-end { align-items: flex-end !important; }
  .align-items-xl-center { align-items: center !important; }
  .align-items-xl-baseline { align-items: baseline !important; }
  .align-items-xl-stretch { align-items: stretch !important; }
  .align-content-xl-start { align-content: flex-start !important; }
  .align-content-xl-end { align-content: flex-end !important; }
  .align-content-xl-center { align-content: center !important; }
  .align-content-xl-between { align-content: space-between !important; }
  .align-content-xl-around { align-content: space-around !important; }
  .align-content-xl-stretch { align-content: stretch !important; }
  .align-self-xl-auto { align-self: auto !important; }
  .align-self-xl-start { align-self: flex-start !important; }
  .align-self-xl-end { align-self: flex-end !important; }
  .align-self-xl-center { align-self: center !important; }
  .align-self-xl-baseline { align-self: baseline !important; }
  .align-self-xl-stretch { align-self: stretch !important; }
}

.float-left { float: left !important; }

.float-right { float: right !important; }

.float-none { float: none !important; }

@media (min-width: 576px) {
  .float-sm-left { float: left !important; }
  .float-sm-right { float: right !important; }
  .float-sm-none { float: none !important; }
}

@media (min-width: 768px) {
  .float-md-left { float: left !important; }
  .float-md-right { float: right !important; }
  .float-md-none { float: none !important; }
}

@media (min-width: 992px) {
  .float-lg-left { float: left !important; }
  .float-lg-right { float: right !important; }
  .float-lg-none { float: none !important; }
}

@media (min-width: 1200px) {
  .float-xl-left { float: left !important; }
  .float-xl-right { float: right !important; }
  .float-xl-none { float: none !important; }
}

.overflow-auto { overflow: auto !important; }

.overflow-hidden { overflow: hidden !important; }

.position-static { position: static !important; }

.position-relative { position: relative !important; }

.position-absolute { position: absolute !important; }

.position-fixed { position: fixed !important; }

.position-sticky { position: sticky !important; }

.fixed-top { position: fixed; top: 0px; right: 0px; left: 0px; z-index: 103=
0; }

.fixed-bottom { position: fixed; right: 0px; bottom: 0px; left: 0px; z-inde=
x: 1030; }

@supports ((position:-webkit-sticky) or (position:sticky)) {
  .sticky-top { position: sticky; top: 0px; z-index: 1020; }
}

.sr-only { position: absolute; width: 1px; height: 1px; padding: 0px; overf=
low: hidden; clip: rect(0px, 0px, 0px, 0px); white-space: nowrap; border: 0=
px; }

.sr-only-focusable:active, .sr-only-focusable:focus { position: static; wid=
th: auto; height: auto; overflow: visible; clip: auto; white-space: normal;=
 }

.shadow-sm { box-shadow: rgba(0, 0, 0, 0.075) 0px 0.125rem 0.25rem !importa=
nt; }

.shadow { box-shadow: rgba(0, 0, 0, 0.15) 0px 0.5rem 1rem !important; }

.shadow-lg { box-shadow: rgba(0, 0, 0, 0.176) 0px 1rem 3rem !important; }

.shadow-none { box-shadow: none !important; }

.w-25 { width: 25% !important; }

.w-50 { width: 50% !important; }

.w-75 { width: 75% !important; }

.w-100 { width: 100% !important; }

.w-auto { width: auto !important; }

.h-25 { height: 25% !important; }

.h-50 { height: 50% !important; }

.h-75 { height: 75% !important; }

.h-100 { height: 100% !important; }

.h-auto { height: auto !important; }

.mw-100 { max-width: 100% !important; }

.mh-100 { max-height: 100% !important; }

.min-vw-100 { min-width: 100vw !important; }

.min-vh-100 { min-height: 100vh !important; }

.vw-100 { width: 100vw !important; }

.vh-100 { height: 100vh !important; }

.stretched-link::after { position: absolute; inset: 0px; z-index: 1; pointe=
r-events: auto; content: ""; background-color: rgba(0, 0, 0, 0); }

.m-0 { margin: 0px !important; }

.mt-0, .my-0 { margin-top: 0px !important; }

.mr-0, .mx-0 { margin-right: 0px !important; }

.mb-0, .my-0 { margin-bottom: 0px !important; }

.ml-0, .mx-0 { margin-left: 0px !important; }

.m-1 { margin: 0.25rem !important; }

.mt-1, .my-1 { margin-top: 0.25rem !important; }

.mr-1, .mx-1 { margin-right: 0.25rem !important; }

.mb-1, .my-1 { margin-bottom: 0.25rem !important; }

.ml-1, .mx-1 { margin-left: 0.25rem !important; }

.m-2 { margin: 0.5rem !important; }

.mt-2, .my-2 { margin-top: 0.5rem !important; }

.mr-2, .mx-2 { margin-right: 0.5rem !important; }

.mb-2, .my-2 { margin-bottom: 0.5rem !important; }

.ml-2, .mx-2 { margin-left: 0.5rem !important; }

.m-3 { margin: 1rem !important; }

.mt-3, .my-3 { margin-top: 1rem !important; }

.mr-3, .mx-3 { margin-right: 1rem !important; }

.mb-3, .my-3 { margin-bottom: 1rem !important; }

.ml-3, .mx-3 { margin-left: 1rem !important; }

.m-4 { margin: 1.5rem !important; }

.mt-4, .my-4 { margin-top: 1.5rem !important; }

.mr-4, .mx-4 { margin-right: 1.5rem !important; }

.mb-4, .my-4 { margin-bottom: 1.5rem !important; }

.ml-4, .mx-4 { margin-left: 1.5rem !important; }

.m-5 { margin: 3rem !important; }

.mt-5, .my-5 { margin-top: 3rem !important; }

.mr-5, .mx-5 { margin-right: 3rem !important; }

.mb-5, .my-5 { margin-bottom: 3rem !important; }

.ml-5, .mx-5 { margin-left: 3rem !important; }

.p-0 { padding: 0px !important; }

.pt-0, .py-0 { padding-top: 0px !important; }

.pr-0, .px-0 { padding-right: 0px !important; }

.pb-0, .py-0 { padding-bottom: 0px !important; }

.pl-0, .px-0 { padding-left: 0px !important; }

.p-1 { padding: 0.25rem !important; }

.pt-1, .py-1 { padding-top: 0.25rem !important; }

.pr-1, .px-1 { padding-right: 0.25rem !important; }

.pb-1, .py-1 { padding-bottom: 0.25rem !important; }

.pl-1, .px-1 { padding-left: 0.25rem !important; }

.p-2 { padding: 0.5rem !important; }

.pt-2, .py-2 { padding-top: 0.5rem !important; }

.pr-2, .px-2 { padding-right: 0.5rem !important; }

.pb-2, .py-2 { padding-bottom: 0.5rem !important; }

.pl-2, .px-2 { padding-left: 0.5rem !important; }

.p-3 { padding: 1rem !important; }

.pt-3, .py-3 { padding-top: 1rem !important; }

.pr-3, .px-3 { padding-right: 1rem !important; }

.pb-3, .py-3 { padding-bottom: 1rem !important; }

.pl-3, .px-3 { padding-left: 1rem !important; }

.p-4 { padding: 1.5rem !important; }

.pt-4, .py-4 { padding-top: 1.5rem !important; }

.pr-4, .px-4 { padding-right: 1.5rem !important; }

.pb-4, .py-4 { padding-bottom: 1.5rem !important; }

.pl-4, .px-4 { padding-left: 1.5rem !important; }

.p-5 { padding: 3rem !important; }

.pt-5, .py-5 { padding-top: 3rem !important; }

.pr-5, .px-5 { padding-right: 3rem !important; }

.pb-5, .py-5 { padding-bottom: 3rem !important; }

.pl-5, .px-5 { padding-left: 3rem !important; }

.m-n1 { margin: -0.25rem !important; }

.mt-n1, .my-n1 { margin-top: -0.25rem !important; }

.mr-n1, .mx-n1 { margin-right: -0.25rem !important; }

.mb-n1, .my-n1 { margin-bottom: -0.25rem !important; }

.ml-n1, .mx-n1 { margin-left: -0.25rem !important; }

.m-n2 { margin: -0.5rem !important; }

.mt-n2, .my-n2 { margin-top: -0.5rem !important; }

.mr-n2, .mx-n2 { margin-right: -0.5rem !important; }

.mb-n2, .my-n2 { margin-bottom: -0.5rem !important; }

.ml-n2, .mx-n2 { margin-left: -0.5rem !important; }

.m-n3 { margin: -1rem !important; }

.mt-n3, .my-n3 { margin-top: -1rem !important; }

.mr-n3, .mx-n3 { margin-right: -1rem !important; }

.mb-n3, .my-n3 { margin-bottom: -1rem !important; }

.ml-n3, .mx-n3 { margin-left: -1rem !important; }

.m-n4 { margin: -1.5rem !important; }

.mt-n4, .my-n4 { margin-top: -1.5rem !important; }

.mr-n4, .mx-n4 { margin-right: -1.5rem !important; }

.mb-n4, .my-n4 { margin-bottom: -1.5rem !important; }

.ml-n4, .mx-n4 { margin-left: -1.5rem !important; }

.m-n5 { margin: -3rem !important; }

.mt-n5, .my-n5 { margin-top: -3rem !important; }

.mr-n5, .mx-n5 { margin-right: -3rem !important; }

.mb-n5, .my-n5 { margin-bottom: -3rem !important; }

.ml-n5, .mx-n5 { margin-left: -3rem !important; }

.m-auto { margin: auto !important; }

.mt-auto, .my-auto { margin-top: auto !important; }

.mr-auto, .mx-auto { margin-right: auto !important; }

.mb-auto, .my-auto { margin-bottom: auto !important; }

.ml-auto, .mx-auto { margin-left: auto !important; }

@media (min-width: 576px) {
  .m-sm-0 { margin: 0px !important; }
  .mt-sm-0, .my-sm-0 { margin-top: 0px !important; }
  .mr-sm-0, .mx-sm-0 { margin-right: 0px !important; }
  .mb-sm-0, .my-sm-0 { margin-bottom: 0px !important; }
  .ml-sm-0, .mx-sm-0 { margin-left: 0px !important; }
  .m-sm-1 { margin: 0.25rem !important; }
  .mt-sm-1, .my-sm-1 { margin-top: 0.25rem !important; }
  .mr-sm-1, .mx-sm-1 { margin-right: 0.25rem !important; }
  .mb-sm-1, .my-sm-1 { margin-bottom: 0.25rem !important; }
  .ml-sm-1, .mx-sm-1 { margin-left: 0.25rem !important; }
  .m-sm-2 { margin: 0.5rem !important; }
  .mt-sm-2, .my-sm-2 { margin-top: 0.5rem !important; }
  .mr-sm-2, .mx-sm-2 { margin-right: 0.5rem !important; }
  .mb-sm-2, .my-sm-2 { margin-bottom: 0.5rem !important; }
  .ml-sm-2, .mx-sm-2 { margin-left: 0.5rem !important; }
  .m-sm-3 { margin: 1rem !important; }
  .mt-sm-3, .my-sm-3 { margin-top: 1rem !important; }
  .mr-sm-3, .mx-sm-3 { margin-right: 1rem !important; }
  .mb-sm-3, .my-sm-3 { margin-bottom: 1rem !important; }
  .ml-sm-3, .mx-sm-3 { margin-left: 1rem !important; }
  .m-sm-4 { margin: 1.5rem !important; }
  .mt-sm-4, .my-sm-4 { margin-top: 1.5rem !important; }
  .mr-sm-4, .mx-sm-4 { margin-right: 1.5rem !important; }
  .mb-sm-4, .my-sm-4 { margin-bottom: 1.5rem !important; }
  .ml-sm-4, .mx-sm-4 { margin-left: 1.5rem !important; }
  .m-sm-5 { margin: 3rem !important; }
  .mt-sm-5, .my-sm-5 { margin-top: 3rem !important; }
  .mr-sm-5, .mx-sm-5 { margin-right: 3rem !important; }
  .mb-sm-5, .my-sm-5 { margin-bottom: 3rem !important; }
  .ml-sm-5, .mx-sm-5 { margin-left: 3rem !important; }
  .p-sm-0 { padding: 0px !important; }
  .pt-sm-0, .py-sm-0 { padding-top: 0px !important; }
  .pr-sm-0, .px-sm-0 { padding-right: 0px !important; }
  .pb-sm-0, .py-sm-0 { padding-bottom: 0px !important; }
  .pl-sm-0, .px-sm-0 { padding-left: 0px !important; }
  .p-sm-1 { padding: 0.25rem !important; }
  .pt-sm-1, .py-sm-1 { padding-top: 0.25rem !important; }
  .pr-sm-1, .px-sm-1 { padding-right: 0.25rem !important; }
  .pb-sm-1, .py-sm-1 { padding-bottom: 0.25rem !important; }
  .pl-sm-1, .px-sm-1 { padding-left: 0.25rem !important; }
  .p-sm-2 { padding: 0.5rem !important; }
  .pt-sm-2, .py-sm-2 { padding-top: 0.5rem !important; }
  .pr-sm-2, .px-sm-2 { padding-right: 0.5rem !important; }
  .pb-sm-2, .py-sm-2 { padding-bottom: 0.5rem !important; }
  .pl-sm-2, .px-sm-2 { padding-left: 0.5rem !important; }
  .p-sm-3 { padding: 1rem !important; }
  .pt-sm-3, .py-sm-3 { padding-top: 1rem !important; }
  .pr-sm-3, .px-sm-3 { padding-right: 1rem !important; }
  .pb-sm-3, .py-sm-3 { padding-bottom: 1rem !important; }
  .pl-sm-3, .px-sm-3 { padding-left: 1rem !important; }
  .p-sm-4 { padding: 1.5rem !important; }
  .pt-sm-4, .py-sm-4 { padding-top: 1.5rem !important; }
  .pr-sm-4, .px-sm-4 { padding-right: 1.5rem !important; }
  .pb-sm-4, .py-sm-4 { padding-bottom: 1.5rem !important; }
  .pl-sm-4, .px-sm-4 { padding-left: 1.5rem !important; }
  .p-sm-5 { padding: 3rem !important; }
  .pt-sm-5, .py-sm-5 { padding-top: 3rem !important; }
  .pr-sm-5, .px-sm-5 { padding-right: 3rem !important; }
  .pb-sm-5, .py-sm-5 { padding-bottom: 3rem !important; }
  .pl-sm-5, .px-sm-5 { padding-left: 3rem !important; }
  .m-sm-n1 { margin: -0.25rem !important; }
  .mt-sm-n1, .my-sm-n1 { margin-top: -0.25rem !important; }
  .mr-sm-n1, .mx-sm-n1 { margin-right: -0.25rem !important; }
  .mb-sm-n1, .my-sm-n1 { margin-bottom: -0.25rem !important; }
  .ml-sm-n1, .mx-sm-n1 { margin-left: -0.25rem !important; }
  .m-sm-n2 { margin: -0.5rem !important; }
  .mt-sm-n2, .my-sm-n2 { margin-top: -0.5rem !important; }
  .mr-sm-n2, .mx-sm-n2 { margin-right: -0.5rem !important; }
  .mb-sm-n2, .my-sm-n2 { margin-bottom: -0.5rem !important; }
  .ml-sm-n2, .mx-sm-n2 { margin-left: -0.5rem !important; }
  .m-sm-n3 { margin: -1rem !important; }
  .mt-sm-n3, .my-sm-n3 { margin-top: -1rem !important; }
  .mr-sm-n3, .mx-sm-n3 { margin-right: -1rem !important; }
  .mb-sm-n3, .my-sm-n3 { margin-bottom: -1rem !important; }
  .ml-sm-n3, .mx-sm-n3 { margin-left: -1rem !important; }
  .m-sm-n4 { margin: -1.5rem !important; }
  .mt-sm-n4, .my-sm-n4 { margin-top: -1.5rem !important; }
  .mr-sm-n4, .mx-sm-n4 { margin-right: -1.5rem !important; }
  .mb-sm-n4, .my-sm-n4 { margin-bottom: -1.5rem !important; }
  .ml-sm-n4, .mx-sm-n4 { margin-left: -1.5rem !important; }
  .m-sm-n5 { margin: -3rem !important; }
  .mt-sm-n5, .my-sm-n5 { margin-top: -3rem !important; }
  .mr-sm-n5, .mx-sm-n5 { margin-right: -3rem !important; }
  .mb-sm-n5, .my-sm-n5 { margin-bottom: -3rem !important; }
  .ml-sm-n5, .mx-sm-n5 { margin-left: -3rem !important; }
  .m-sm-auto { margin: auto !important; }
  .mt-sm-auto, .my-sm-auto { margin-top: auto !important; }
  .mr-sm-auto, .mx-sm-auto { margin-right: auto !important; }
  .mb-sm-auto, .my-sm-auto { margin-bottom: auto !important; }
  .ml-sm-auto, .mx-sm-auto { margin-left: auto !important; }
}

@media (min-width: 768px) {
  .m-md-0 { margin: 0px !important; }
  .mt-md-0, .my-md-0 { margin-top: 0px !important; }
  .mr-md-0, .mx-md-0 { margin-right: 0px !important; }
  .mb-md-0, .my-md-0 { margin-bottom: 0px !important; }
  .ml-md-0, .mx-md-0 { margin-left: 0px !important; }
  .m-md-1 { margin: 0.25rem !important; }
  .mt-md-1, .my-md-1 { margin-top: 0.25rem !important; }
  .mr-md-1, .mx-md-1 { margin-right: 0.25rem !important; }
  .mb-md-1, .my-md-1 { margin-bottom: 0.25rem !important; }
  .ml-md-1, .mx-md-1 { margin-left: 0.25rem !important; }
  .m-md-2 { margin: 0.5rem !important; }
  .mt-md-2, .my-md-2 { margin-top: 0.5rem !important; }
  .mr-md-2, .mx-md-2 { margin-right: 0.5rem !important; }
  .mb-md-2, .my-md-2 { margin-bottom: 0.5rem !important; }
  .ml-md-2, .mx-md-2 { margin-left: 0.5rem !important; }
  .m-md-3 { margin: 1rem !important; }
  .mt-md-3, .my-md-3 { margin-top: 1rem !important; }
  .mr-md-3, .mx-md-3 { margin-right: 1rem !important; }
  .mb-md-3, .my-md-3 { margin-bottom: 1rem !important; }
  .ml-md-3, .mx-md-3 { margin-left: 1rem !important; }
  .m-md-4 { margin: 1.5rem !important; }
  .mt-md-4, .my-md-4 { margin-top: 1.5rem !important; }
  .mr-md-4, .mx-md-4 { margin-right: 1.5rem !important; }
  .mb-md-4, .my-md-4 { margin-bottom: 1.5rem !important; }
  .ml-md-4, .mx-md-4 { margin-left: 1.5rem !important; }
  .m-md-5 { margin: 3rem !important; }
  .mt-md-5, .my-md-5 { margin-top: 3rem !important; }
  .mr-md-5, .mx-md-5 { margin-right: 3rem !important; }
  .mb-md-5, .my-md-5 { margin-bottom: 3rem !important; }
  .ml-md-5, .mx-md-5 { margin-left: 3rem !important; }
  .p-md-0 { padding: 0px !important; }
  .pt-md-0, .py-md-0 { padding-top: 0px !important; }
  .pr-md-0, .px-md-0 { padding-right: 0px !important; }
  .pb-md-0, .py-md-0 { padding-bottom: 0px !important; }
  .pl-md-0, .px-md-0 { padding-left: 0px !important; }
  .p-md-1 { padding: 0.25rem !important; }
  .pt-md-1, .py-md-1 { padding-top: 0.25rem !important; }
  .pr-md-1, .px-md-1 { padding-right: 0.25rem !important; }
  .pb-md-1, .py-md-1 { padding-bottom: 0.25rem !important; }
  .pl-md-1, .px-md-1 { padding-left: 0.25rem !important; }
  .p-md-2 { padding: 0.5rem !important; }
  .pt-md-2, .py-md-2 { padding-top: 0.5rem !important; }
  .pr-md-2, .px-md-2 { padding-right: 0.5rem !important; }
  .pb-md-2, .py-md-2 { padding-bottom: 0.5rem !important; }
  .pl-md-2, .px-md-2 { padding-left: 0.5rem !important; }
  .p-md-3 { padding: 1rem !important; }
  .pt-md-3, .py-md-3 { padding-top: 1rem !important; }
  .pr-md-3, .px-md-3 { padding-right: 1rem !important; }
  .pb-md-3, .py-md-3 { padding-bottom: 1rem !important; }
  .pl-md-3, .px-md-3 { padding-left: 1rem !important; }
  .p-md-4 { padding: 1.5rem !important; }
  .pt-md-4, .py-md-4 { padding-top: 1.5rem !important; }
  .pr-md-4, .px-md-4 { padding-right: 1.5rem !important; }
  .pb-md-4, .py-md-4 { padding-bottom: 1.5rem !important; }
  .pl-md-4, .px-md-4 { padding-left: 1.5rem !important; }
  .p-md-5 { padding: 3rem !important; }
  .pt-md-5, .py-md-5 { padding-top: 3rem !important; }
  .pr-md-5, .px-md-5 { padding-right: 3rem !important; }
  .pb-md-5, .py-md-5 { padding-bottom: 3rem !important; }
  .pl-md-5, .px-md-5 { padding-left: 3rem !important; }
  .m-md-n1 { margin: -0.25rem !important; }
  .mt-md-n1, .my-md-n1 { margin-top: -0.25rem !important; }
  .mr-md-n1, .mx-md-n1 { margin-right: -0.25rem !important; }
  .mb-md-n1, .my-md-n1 { margin-bottom: -0.25rem !important; }
  .ml-md-n1, .mx-md-n1 { margin-left: -0.25rem !important; }
  .m-md-n2 { margin: -0.5rem !important; }
  .mt-md-n2, .my-md-n2 { margin-top: -0.5rem !important; }
  .mr-md-n2, .mx-md-n2 { margin-right: -0.5rem !important; }
  .mb-md-n2, .my-md-n2 { margin-bottom: -0.5rem !important; }
  .ml-md-n2, .mx-md-n2 { margin-left: -0.5rem !important; }
  .m-md-n3 { margin: -1rem !important; }
  .mt-md-n3, .my-md-n3 { margin-top: -1rem !important; }
  .mr-md-n3, .mx-md-n3 { margin-right: -1rem !important; }
  .mb-md-n3, .my-md-n3 { margin-bottom: -1rem !important; }
  .ml-md-n3, .mx-md-n3 { margin-left: -1rem !important; }
  .m-md-n4 { margin: -1.5rem !important; }
  .mt-md-n4, .my-md-n4 { margin-top: -1.5rem !important; }
  .mr-md-n4, .mx-md-n4 { margin-right: -1.5rem !important; }
  .mb-md-n4, .my-md-n4 { margin-bottom: -1.5rem !important; }
  .ml-md-n4, .mx-md-n4 { margin-left: -1.5rem !important; }
  .m-md-n5 { margin: -3rem !important; }
  .mt-md-n5, .my-md-n5 { margin-top: -3rem !important; }
  .mr-md-n5, .mx-md-n5 { margin-right: -3rem !important; }
  .mb-md-n5, .my-md-n5 { margin-bottom: -3rem !important; }
  .ml-md-n5, .mx-md-n5 { margin-left: -3rem !important; }
  .m-md-auto { margin: auto !important; }
  .mt-md-auto, .my-md-auto { margin-top: auto !important; }
  .mr-md-auto, .mx-md-auto { margin-right: auto !important; }
  .mb-md-auto, .my-md-auto { margin-bottom: auto !important; }
  .ml-md-auto, .mx-md-auto { margin-left: auto !important; }
}

@media (min-width: 992px) {
  .m-lg-0 { margin: 0px !important; }
  .mt-lg-0, .my-lg-0 { margin-top: 0px !important; }
  .mr-lg-0, .mx-lg-0 { margin-right: 0px !important; }
  .mb-lg-0, .my-lg-0 { margin-bottom: 0px !important; }
  .ml-lg-0, .mx-lg-0 { margin-left: 0px !important; }
  .m-lg-1 { margin: 0.25rem !important; }
  .mt-lg-1, .my-lg-1 { margin-top: 0.25rem !important; }
  .mr-lg-1, .mx-lg-1 { margin-right: 0.25rem !important; }
  .mb-lg-1, .my-lg-1 { margin-bottom: 0.25rem !important; }
  .ml-lg-1, .mx-lg-1 { margin-left: 0.25rem !important; }
  .m-lg-2 { margin: 0.5rem !important; }
  .mt-lg-2, .my-lg-2 { margin-top: 0.5rem !important; }
  .mr-lg-2, .mx-lg-2 { margin-right: 0.5rem !important; }
  .mb-lg-2, .my-lg-2 { margin-bottom: 0.5rem !important; }
  .ml-lg-2, .mx-lg-2 { margin-left: 0.5rem !important; }
  .m-lg-3 { margin: 1rem !important; }
  .mt-lg-3, .my-lg-3 { margin-top: 1rem !important; }
  .mr-lg-3, .mx-lg-3 { margin-right: 1rem !important; }
  .mb-lg-3, .my-lg-3 { margin-bottom: 1rem !important; }
  .ml-lg-3, .mx-lg-3 { margin-left: 1rem !important; }
  .m-lg-4 { margin: 1.5rem !important; }
  .mt-lg-4, .my-lg-4 { margin-top: 1.5rem !important; }
  .mr-lg-4, .mx-lg-4 { margin-right: 1.5rem !important; }
  .mb-lg-4, .my-lg-4 { margin-bottom: 1.5rem !important; }
  .ml-lg-4, .mx-lg-4 { margin-left: 1.5rem !important; }
  .m-lg-5 { margin: 3rem !important; }
  .mt-lg-5, .my-lg-5 { margin-top: 3rem !important; }
  .mr-lg-5, .mx-lg-5 { margin-right: 3rem !important; }
  .mb-lg-5, .my-lg-5 { margin-bottom: 3rem !important; }
  .ml-lg-5, .mx-lg-5 { margin-left: 3rem !important; }
  .p-lg-0 { padding: 0px !important; }
  .pt-lg-0, .py-lg-0 { padding-top: 0px !important; }
  .pr-lg-0, .px-lg-0 { padding-right: 0px !important; }
  .pb-lg-0, .py-lg-0 { padding-bottom: 0px !important; }
  .pl-lg-0, .px-lg-0 { padding-left: 0px !important; }
  .p-lg-1 { padding: 0.25rem !important; }
  .pt-lg-1, .py-lg-1 { padding-top: 0.25rem !important; }
  .pr-lg-1, .px-lg-1 { padding-right: 0.25rem !important; }
  .pb-lg-1, .py-lg-1 { padding-bottom: 0.25rem !important; }
  .pl-lg-1, .px-lg-1 { padding-left: 0.25rem !important; }
  .p-lg-2 { padding: 0.5rem !important; }
  .pt-lg-2, .py-lg-2 { padding-top: 0.5rem !important; }
  .pr-lg-2, .px-lg-2 { padding-right: 0.5rem !important; }
  .pb-lg-2, .py-lg-2 { padding-bottom: 0.5rem !important; }
  .pl-lg-2, .px-lg-2 { padding-left: 0.5rem !important; }
  .p-lg-3 { padding: 1rem !important; }
  .pt-lg-3, .py-lg-3 { padding-top: 1rem !important; }
  .pr-lg-3, .px-lg-3 { padding-right: 1rem !important; }
  .pb-lg-3, .py-lg-3 { padding-bottom: 1rem !important; }
  .pl-lg-3, .px-lg-3 { padding-left: 1rem !important; }
  .p-lg-4 { padding: 1.5rem !important; }
  .pt-lg-4, .py-lg-4 { padding-top: 1.5rem !important; }
  .pr-lg-4, .px-lg-4 { padding-right: 1.5rem !important; }
  .pb-lg-4, .py-lg-4 { padding-bottom: 1.5rem !important; }
  .pl-lg-4, .px-lg-4 { padding-left: 1.5rem !important; }
  .p-lg-5 { padding: 3rem !important; }
  .pt-lg-5, .py-lg-5 { padding-top: 3rem !important; }
  .pr-lg-5, .px-lg-5 { padding-right: 3rem !important; }
  .pb-lg-5, .py-lg-5 { padding-bottom: 3rem !important; }
  .pl-lg-5, .px-lg-5 { padding-left: 3rem !important; }
  .m-lg-n1 { margin: -0.25rem !important; }
  .mt-lg-n1, .my-lg-n1 { margin-top: -0.25rem !important; }
  .mr-lg-n1, .mx-lg-n1 { margin-right: -0.25rem !important; }
  .mb-lg-n1, .my-lg-n1 { margin-bottom: -0.25rem !important; }
  .ml-lg-n1, .mx-lg-n1 { margin-left: -0.25rem !important; }
  .m-lg-n2 { margin: -0.5rem !important; }
  .mt-lg-n2, .my-lg-n2 { margin-top: -0.5rem !important; }
  .mr-lg-n2, .mx-lg-n2 { margin-right: -0.5rem !important; }
  .mb-lg-n2, .my-lg-n2 { margin-bottom: -0.5rem !important; }
  .ml-lg-n2, .mx-lg-n2 { margin-left: -0.5rem !important; }
  .m-lg-n3 { margin: -1rem !important; }
  .mt-lg-n3, .my-lg-n3 { margin-top: -1rem !important; }
  .mr-lg-n3, .mx-lg-n3 { margin-right: -1rem !important; }
  .mb-lg-n3, .my-lg-n3 { margin-bottom: -1rem !important; }
  .ml-lg-n3, .mx-lg-n3 { margin-left: -1rem !important; }
  .m-lg-n4 { margin: -1.5rem !important; }
  .mt-lg-n4, .my-lg-n4 { margin-top: -1.5rem !important; }
  .mr-lg-n4, .mx-lg-n4 { margin-right: -1.5rem !important; }
  .mb-lg-n4, .my-lg-n4 { margin-bottom: -1.5rem !important; }
  .ml-lg-n4, .mx-lg-n4 { margin-left: -1.5rem !important; }
  .m-lg-n5 { margin: -3rem !important; }
  .mt-lg-n5, .my-lg-n5 { margin-top: -3rem !important; }
  .mr-lg-n5, .mx-lg-n5 { margin-right: -3rem !important; }
  .mb-lg-n5, .my-lg-n5 { margin-bottom: -3rem !important; }
  .ml-lg-n5, .mx-lg-n5 { margin-left: -3rem !important; }
  .m-lg-auto { margin: auto !important; }
  .mt-lg-auto, .my-lg-auto { margin-top: auto !important; }
  .mr-lg-auto, .mx-lg-auto { margin-right: auto !important; }
  .mb-lg-auto, .my-lg-auto { margin-bottom: auto !important; }
  .ml-lg-auto, .mx-lg-auto { margin-left: auto !important; }
}

@media (min-width: 1200px) {
  .m-xl-0 { margin: 0px !important; }
  .mt-xl-0, .my-xl-0 { margin-top: 0px !important; }
  .mr-xl-0, .mx-xl-0 { margin-right: 0px !important; }
  .mb-xl-0, .my-xl-0 { margin-bottom: 0px !important; }
  .ml-xl-0, .mx-xl-0 { margin-left: 0px !important; }
  .m-xl-1 { margin: 0.25rem !important; }
  .mt-xl-1, .my-xl-1 { margin-top: 0.25rem !important; }
  .mr-xl-1, .mx-xl-1 { margin-right: 0.25rem !important; }
  .mb-xl-1, .my-xl-1 { margin-bottom: 0.25rem !important; }
  .ml-xl-1, .mx-xl-1 { margin-left: 0.25rem !important; }
  .m-xl-2 { margin: 0.5rem !important; }
  .mt-xl-2, .my-xl-2 { margin-top: 0.5rem !important; }
  .mr-xl-2, .mx-xl-2 { margin-right: 0.5rem !important; }
  .mb-xl-2, .my-xl-2 { margin-bottom: 0.5rem !important; }
  .ml-xl-2, .mx-xl-2 { margin-left: 0.5rem !important; }
  .m-xl-3 { margin: 1rem !important; }
  .mt-xl-3, .my-xl-3 { margin-top: 1rem !important; }
  .mr-xl-3, .mx-xl-3 { margin-right: 1rem !important; }
  .mb-xl-3, .my-xl-3 { margin-bottom: 1rem !important; }
  .ml-xl-3, .mx-xl-3 { margin-left: 1rem !important; }
  .m-xl-4 { margin: 1.5rem !important; }
  .mt-xl-4, .my-xl-4 { margin-top: 1.5rem !important; }
  .mr-xl-4, .mx-xl-4 { margin-right: 1.5rem !important; }
  .mb-xl-4, .my-xl-4 { margin-bottom: 1.5rem !important; }
  .ml-xl-4, .mx-xl-4 { margin-left: 1.5rem !important; }
  .m-xl-5 { margin: 3rem !important; }
  .mt-xl-5, .my-xl-5 { margin-top: 3rem !important; }
  .mr-xl-5, .mx-xl-5 { margin-right: 3rem !important; }
  .mb-xl-5, .my-xl-5 { margin-bottom: 3rem !important; }
  .ml-xl-5, .mx-xl-5 { margin-left: 3rem !important; }
  .p-xl-0 { padding: 0px !important; }
  .pt-xl-0, .py-xl-0 { padding-top: 0px !important; }
  .pr-xl-0, .px-xl-0 { padding-right: 0px !important; }
  .pb-xl-0, .py-xl-0 { padding-bottom: 0px !important; }
  .pl-xl-0, .px-xl-0 { padding-left: 0px !important; }
  .p-xl-1 { padding: 0.25rem !important; }
  .pt-xl-1, .py-xl-1 { padding-top: 0.25rem !important; }
  .pr-xl-1, .px-xl-1 { padding-right: 0.25rem !important; }
  .pb-xl-1, .py-xl-1 { padding-bottom: 0.25rem !important; }
  .pl-xl-1, .px-xl-1 { padding-left: 0.25rem !important; }
  .p-xl-2 { padding: 0.5rem !important; }
  .pt-xl-2, .py-xl-2 { padding-top: 0.5rem !important; }
  .pr-xl-2, .px-xl-2 { padding-right: 0.5rem !important; }
  .pb-xl-2, .py-xl-2 { padding-bottom: 0.5rem !important; }
  .pl-xl-2, .px-xl-2 { padding-left: 0.5rem !important; }
  .p-xl-3 { padding: 1rem !important; }
  .pt-xl-3, .py-xl-3 { padding-top: 1rem !important; }
  .pr-xl-3, .px-xl-3 { padding-right: 1rem !important; }
  .pb-xl-3, .py-xl-3 { padding-bottom: 1rem !important; }
  .pl-xl-3, .px-xl-3 { padding-left: 1rem !important; }
  .p-xl-4 { padding: 1.5rem !important; }
  .pt-xl-4, .py-xl-4 { padding-top: 1.5rem !important; }
  .pr-xl-4, .px-xl-4 { padding-right: 1.5rem !important; }
  .pb-xl-4, .py-xl-4 { padding-bottom: 1.5rem !important; }
  .pl-xl-4, .px-xl-4 { padding-left: 1.5rem !important; }
  .p-xl-5 { padding: 3rem !important; }
  .pt-xl-5, .py-xl-5 { padding-top: 3rem !important; }
  .pr-xl-5, .px-xl-5 { padding-right: 3rem !important; }
  .pb-xl-5, .py-xl-5 { padding-bottom: 3rem !important; }
  .pl-xl-5, .px-xl-5 { padding-left: 3rem !important; }
  .m-xl-n1 { margin: -0.25rem !important; }
  .mt-xl-n1, .my-xl-n1 { margin-top: -0.25rem !important; }
  .mr-xl-n1, .mx-xl-n1 { margin-right: -0.25rem !important; }
  .mb-xl-n1, .my-xl-n1 { margin-bottom: -0.25rem !important; }
  .ml-xl-n1, .mx-xl-n1 { margin-left: -0.25rem !important; }
  .m-xl-n2 { margin: -0.5rem !important; }
  .mt-xl-n2, .my-xl-n2 { margin-top: -0.5rem !important; }
  .mr-xl-n2, .mx-xl-n2 { margin-right: -0.5rem !important; }
  .mb-xl-n2, .my-xl-n2 { margin-bottom: -0.5rem !important; }
  .ml-xl-n2, .mx-xl-n2 { margin-left: -0.5rem !important; }
  .m-xl-n3 { margin: -1rem !important; }
  .mt-xl-n3, .my-xl-n3 { margin-top: -1rem !important; }
  .mr-xl-n3, .mx-xl-n3 { margin-right: -1rem !important; }
  .mb-xl-n3, .my-xl-n3 { margin-bottom: -1rem !important; }
  .ml-xl-n3, .mx-xl-n3 { margin-left: -1rem !important; }
  .m-xl-n4 { margin: -1.5rem !important; }
  .mt-xl-n4, .my-xl-n4 { margin-top: -1.5rem !important; }
  .mr-xl-n4, .mx-xl-n4 { margin-right: -1.5rem !important; }
  .mb-xl-n4, .my-xl-n4 { margin-bottom: -1.5rem !important; }
  .ml-xl-n4, .mx-xl-n4 { margin-left: -1.5rem !important; }
  .m-xl-n5 { margin: -3rem !important; }
  .mt-xl-n5, .my-xl-n5 { margin-top: -3rem !important; }
  .mr-xl-n5, .mx-xl-n5 { margin-right: -3rem !important; }
  .mb-xl-n5, .my-xl-n5 { margin-bottom: -3rem !important; }
  .ml-xl-n5, .mx-xl-n5 { margin-left: -3rem !important; }
  .m-xl-auto { margin: auto !important; }
  .mt-xl-auto, .my-xl-auto { margin-top: auto !important; }
  .mr-xl-auto, .mx-xl-auto { margin-right: auto !important; }
  .mb-xl-auto, .my-xl-auto { margin-bottom: auto !important; }
  .ml-xl-auto, .mx-xl-auto { margin-left: auto !important; }
}

.text-monospace { font-family: SFMono-Regular, Menlo, Monaco, Consolas, "Li=
beration Mono", "Courier New", monospace !important; }

.text-justify { text-align: justify !important; }

.text-wrap { white-space: normal !important; }

.text-nowrap { white-space: nowrap !important; }

.text-truncate { overflow: hidden; text-overflow: ellipsis; white-space: no=
wrap; }

.text-left { text-align: left !important; }

.text-right { text-align: right !important; }

.text-center { text-align: center !important; }

@media (min-width: 576px) {
  .text-sm-left { text-align: left !important; }
  .text-sm-right { text-align: right !important; }
  .text-sm-center { text-align: center !important; }
}

@media (min-width: 768px) {
  .text-md-left { text-align: left !important; }
  .text-md-right { text-align: right !important; }
  .text-md-center { text-align: center !important; }
}

@media (min-width: 992px) {
  .text-lg-left { text-align: left !important; }
  .text-lg-right { text-align: right !important; }
  .text-lg-center { text-align: center !important; }
}

@media (min-width: 1200px) {
  .text-xl-left { text-align: left !important; }
  .text-xl-right { text-align: right !important; }
  .text-xl-center { text-align: center !important; }
}

.text-lowercase { text-transform: lowercase !important; }

.text-uppercase { text-transform: uppercase !important; }

.text-capitalize { text-transform: capitalize !important; }

.font-weight-light { font-weight: 300 !important; }

.font-weight-lighter { font-weight: lighter !important; }

.font-weight-normal { font-weight: 400 !important; }

.font-weight-bold { font-weight: 700 !important; }

.font-weight-bolder { font-weight: bolder !important; }

.font-italic { font-style: italic !important; }

.text-white { color: rgb(255, 255, 255) !important; }

.text-primary { color: rgb(0, 123, 255) !important; }

a.text-primary:focus, a.text-primary:hover { color: rgb(0, 86, 179) !import=
ant; }

.text-secondary { color: rgb(108, 117, 125) !important; }

a.text-secondary:focus, a.text-secondary:hover { color: rgb(73, 79, 84) !im=
portant; }

.text-success { color: rgb(40, 167, 69) !important; }

a.text-success:focus, a.text-success:hover { color: rgb(25, 105, 44) !impor=
tant; }

.text-info { color: rgb(23, 162, 184) !important; }

a.text-info:focus, a.text-info:hover { color: rgb(15, 102, 116) !important;=
 }

.text-warning { color: rgb(255, 193, 7) !important; }

a.text-warning:focus, a.text-warning:hover { color: rgb(186, 139, 0) !impor=
tant; }

.text-danger { color: rgb(220, 53, 69) !important; }

a.text-danger:focus, a.text-danger:hover { color: rgb(167, 29, 42) !importa=
nt; }

.text-light { color: rgb(248, 249, 250) !important; }

a.text-light:focus, a.text-light:hover { color: rgb(203, 211, 218) !importa=
nt; }

.text-dark { color: rgb(52, 58, 64) !important; }

a.text-dark:focus, a.text-dark:hover { color: rgb(18, 20, 22) !important; }

.text-body { color: rgb(33, 37, 41) !important; }

.text-muted { color: rgb(108, 117, 125) !important; }

.text-black-50 { color: rgba(0, 0, 0, 0.5) !important; }

.text-white-50 { color: rgba(255, 255, 255, 0.5) !important; }

.text-hide { font: 0px / 0 a; color: transparent; text-shadow: none; backgr=
ound-color: transparent; border: 0px; }

.text-decoration-none { text-decoration: none !important; }

.text-break { word-break: break-word !important; overflow-wrap: break-word =
!important; }

.text-reset { color: inherit !important; }

.visible { visibility: visible !important; }

.invisible { visibility: hidden !important; }

@media print {
  *, ::after, ::before { text-shadow: none !important; box-shadow: none !im=
portant; }
  a:not(.btn) { text-decoration: underline; }
  abbr[title]::after { content: " (" attr(title) ")"; }
  pre { white-space: pre-wrap !important; }
  blockquote, pre { border: 1px solid rgb(173, 181, 189); break-inside: avo=
id; }
  thead { display: table-header-group; }
  img, tr { break-inside: avoid; }
  h2, h3, p { orphans: 3; widows: 3; }
  h2, h3 { break-after: avoid; }
  @page { size: a3; }
  body { min-width: 992px !important; }
  .container { min-width: 992px !important; }
  .navbar { display: none; }
  .badge { border: 1px solid rgb(0, 0, 0); }
  .table { border-collapse: collapse !important; }
  .table td, .table th { background-color: rgb(255, 255, 255) !important; }
  .table-bordered td, .table-bordered th { border: 1px solid rgb(222, 226, =
230) !important; }
  .table-dark { color: inherit; }
  .table-dark tbody + tbody, .table-dark td, .table-dark th, .table-dark th=
ead th { border-color: rgb(222, 226, 230); }
  .table .thead-dark th { color: inherit; border-color: rgb(222, 226, 230);=
 }
}
------MultipartBoundary--ZeJbom7ua2thyClsILZ3bxA8NwD3gXWgKq2ZLWICWB----
Content-Type: text/css
Content-Transfer-Encoding: quoted-printable
Content-Location: https://unpkg.com/@highlightjs/cdn-assets@10.7.1/styles/default.min.css

@charset "utf-8";

.hljs { display: block; overflow-x: auto; padding: 0.5em; background: rgb(2=
40, 240, 240); }

.hljs, .hljs-subst { color: rgb(68, 68, 68); }

.hljs-comment { color: rgb(136, 136, 136); }

.hljs-attribute, .hljs-doctag, .hljs-keyword, .hljs-meta-keyword, .hljs-nam=
e, .hljs-selector-tag { font-weight: 700; }

.hljs-deletion, .hljs-number, .hljs-quote, .hljs-selector-class, .hljs-sele=
ctor-id, .hljs-string, .hljs-template-tag, .hljs-type { color: rgb(136, 0, =
0); }

.hljs-section, .hljs-title { color: rgb(136, 0, 0); font-weight: 700; }

.hljs-link, .hljs-regexp, .hljs-selector-attr, .hljs-selector-pseudo, .hljs=
-symbol, .hljs-template-variable, .hljs-variable { color: rgb(188, 96, 96);=
 }

.hljs-literal { color: rgb(120, 169, 96); }

.hljs-addition, .hljs-built_in, .hljs-bullet, .hljs-code { color: rgb(57, 1=
15, 0); }

.hljs-meta { color: rgb(31, 113, 153); }

.hljs-meta-string { color: rgb(77, 153, 191); }

.hljs-emphasis { font-style: italic; }

.hljs-strong { font-weight: 700; }
------MultipartBoundary--ZeJbom7ua2thyClsILZ3bxA8NwD3gXWgKq2ZLWICWB----
Content-Type: image/png
Content-Transfer-Encoding: base64
Content-Location: https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-DB0201EN-SkillsNetwork/labs/MySQL/week6/images/IDSNlogo.png

iVBORw0KGgoAAAANSUhEUgAAAyAAAAMgCAMAAADsrvZaAAAABGdBTUEAALGPC/xhBQAAAAFzUkdC
AK7OHOkAAADwUExURQAAABdEaCFieBJFaQk4ZhhgjQM1ZiRJZzJmdgU3ZxBCaRlTfBNFafiZORZq
nhZqnhZtoRZqnh1HZxZqntl/QSBIaOViRm+7ThdqnazPOBZqnhZsn9s3TFSxXtw0TlGuR8u6Outk
Ns63PK3QN/rCLvBVNEucTuKkP0OdSd0VbPBlNq3QOPFaNCSy3ie+4GK8h98VbJAwT+alPmK8h6Ee
Sli6R+akPiSw22O8h12zhFi5R+83NCCY0WO9iK5vRie+4IaqRBZJahZqngAzZq7ROVm6R/FmNkSi
Rye+4O43NN4VbN2nQ6IcRWS9iCCX1GS+iL2ocP0AAABBdFJOUwBsEppAIoF/CL/wMtf+ZNFR31rv
Ek0hKZ3pgbg4Ulx6R81olv6got3J0u/KeGLsrpaVt4XM0I+T6dDu0dj2wL7CK2PK9gAAIABJREFU
eNrtnQlj2za2hcVNgkQ9L9Tm2LKs2BMlTZymTlKnSdo0ibt3Ov3//+YBJCVxAUAQXERK5+S9aeJF
C4WPB/fi4qLTgSAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAI
giAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAI
giAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAI
giAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgg5GBJcAgpIaj8fT
mOgXcFUgqEMIg2NJdR0V/TeDhMBQoIN2jinj4p7qdVz3vignU1wk6HD5WF7fv3769O+kwq88ffr6
/noKE4EOVD4ef0tFEVkiGoEOUtPrLDwCRJbwEOgw+fhbRU/hIdAhxh/X90//ViQEkTp0eICo8vH3
36+XuFzQwc2wXqvy8fdTRCHQwRnIMgcgyPVCByYyvX6qDgjCdKhBY3ccalMVNfb/Z1zmXZws7wEI
1Mapz3y+WNwyPYmI/XuxmE9LG6fjXIC8vgYg0O7D5vmCUfFxoz8//vnnx4h8VBbT2gH5G4BAO3eO
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
w5ASTrmNOKy5l4Akckb1AuKIQo2BMEavH5DIRBuHeKYHtiGaDe8LIMYOAdmCYAhe1KCze0AigboL
QDri+0d3LwGJW0jNgPRFHAyEz1A/IJEVsT1bL7SzdpT1Y5frQVLOFx9Bfe5XH1TUVXphHECK7Cjs
y5Y7DO43+iqvsC8Lu7NydH3Rg/Wlz9LVu8Jd0UfazXjZ/Zz7Kdskdw8AcSsHJJKqawMghlK3KwCi
pIyLGebtGg2I4nsoAojdKkA4BWScJhYApARC1mOr2YCovYcigES/3QJA5IRYHQBSEiGbsdVwQJTe
QyFA7HYBIiPE6gCQkgjZjq2mA6LyHgoBEvl+KwARE2J1AEhJhETGVuMBUXgPxQBxWgaIiBCrA0BK
IiQ6tpoPSPZ7KAbIdsC1BBA+IVYHgGhle+20omMr+b3tcqmZ/kX+I3IfhytH8LgZrzHrPeS8AqnF
4tQ3XJVXmF5YdtRfpCt6MDfzWQQXm/eG7ESRKP8bkpft2qKHgiAIgiAIgiAIgiAIgiAIgiAIgiAI
giAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAI
giAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAI
giAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAIgiAI
giAIgiAIgiAIgiAIgiAIgiAIgqD91/8DNX2TMDVdZOgAAAAASUVORK5CYII=

------MultipartBoundary--ZeJbom7ua2thyClsILZ3bxA8NwD3gXWgKq2ZLWICWB----
Content-Type: image/png
Content-Transfer-Encoding: base64
Content-Location: https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-DB0110EN-SkillsNetwork/labs/Lab%20-%20Create%20Tables%20and%20Load%20Data%20in%20MySQL%20using%20phpMyAdmin/images/mysql.png

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
AElFTkSuQmCC

------MultipartBoundary--ZeJbom7ua2thyClsILZ3bxA8NwD3gXWgKq2ZLWICWB----
Content-Type: image/png
Content-Transfer-Encoding: base64
Content-Location: https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-DB0201EN-SkillsNetwork/labs/MySQL/week6/images/1.1.png

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
HD08OJ+3r6NlUrkPefM8/O9Nzjq8Mv9SdpkmO5/PTatjP5+bn1/mHKJrdHXgPEo1AchtYdd1z2mk
/u5nzj3vvP/UqAsudtJ0/awlpNw5lXrIuced/x+mjJP+rk5vxpfpQwIAIBf1L+ix+2J9y7YT33TP
9V4VSjf9Z8gv2MxaVmvO1X6Z2PT1Xwcf5pmyjsh4WPKKLP678OVdHvnjsFvtLc86JQ/o/Xfjl+Gl
d3d3RqqDJiRvNb1si03n/I0efOXrurijQ8d9/j/1+rcvDy/XS+qPsOX1mtI+jqntd7+seRG7jGDy
iqSyvB1vtzglD2p/sl+pOMcxLODhJm81qR3HXlJfhS0rpZQwv8042KFhn/+yc9wadff3fh35Q9qf
wS//rnk4Yx5COXlL/yGwb78RnSeazJz9v06bfzhdD+o23T7lxIRpzv9WfH76qT/Cltd7iswcl+8l
b1pw2V6WeREsZ35RuqBqiRuMnXCKlxd/3GLSu6e7NWcKCmIfcjWve8hdxhUnveuMd2r0laaJq3n6
r9AHWN7yzYoSp9mJi24LPe7h94LUUn+ELa/3FJk5Lt+kd3VGsdmRh7kPBk2eu99X/5vKQ9/3nVrZ
Fp2/x2NkUzrLi5nPXXD4svu6zFRSX4Utq9fU9oZed+Y9+GHYDxBMcu7hMfd3b13mhblm/uue53Tl
PbX6wrHbtX27k479vNcE4z2PR87P5nX/Jc34+2gZJ11krgu1aqu/n9yF3qavTT7aK7Mj2fYkT/0R
trzeU2TmuPzY1PzL77o1FJ6/42PR93+H+Xz/Ly35tX//NgsytV9tGbdJDJPnmPEPut7uu2M+PdH9
3Ljynn+Py3tOrR12nW3eQ+t7p0bXt/3YUk1yLrOmbabPi061b98rtyGeg+8708N/mNBb6quwZfWe
duqNNc7MB95P/t3w3Q617XD2m/+9su3XWrLU2X2PfF0X+fvh4q+7TUgufdh81qa6H15So1nOVz6v
Y/zlbP+YG9DW29uin/Ou2Hntie2+frejTdvf95oj2b/Xa86k+8XHdbc5VquTbWPs8qJpp1qfc86D
4o/Y7fHme/2VRbrVPqzf8aJXM+a2i+10J8WeK+/qeFM7Rg+pMfD5tOPF32q1/xnW6z505gkpc8zk
u71gkiO6zXHJf++1/n49Wtct8r73Ru+77iLMSHQ+PzNSJrX7kGvGV3SdLdPufD/1Pp9/q99H7tfO
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
co96WYv/6uv62Ywl2nTzaQo53XV89/O6Y+JcHaxeptor/V9m9bTfP9Tqf71W1XHXf4y//b5+96WL
7UhqhuQY9XAOT3/kZf3T6MD57ki+3y3/XuW87Kns5f+4TN/53MlpLS/K7v/zF+l3t4y0eVF9W2bv
huJ+Zpwy4iwd2/zdhGvIHJ+7xsR/b1Dkvm2uvQ+f+Iou+6foiWquu0XXHmGP6fE69cw3dN+FU+X2
++z6O/189Xl6YEK1uv91mWquODnxnpqmITmve7jvx3A/z/9X9zr3+8g+cL/nTNbwt7d594u4/eoJ
uz94eQquM347nHv9Mf/va84xsc0LOSb8+2rNfH2Cc/+/VT/970oVm+Oy7f/q4lvM4+PAZ0iKhuo8
9T47d+vRkO9Gpvmpf/7kh3rX36cOc17/6fvOd5Poyeee09+60P9eksJ+MMfvzz/QeTd7j9pdVUv1
/Pk/cvZxt/5t2Rxd6cxzyohh+vVXnO3yd/ttdXr+gp/osievDHz2H6G1s/7KK+Pevy9zro+T9PL3
gtt4he5d/WNdd3z4dyeP+d71qr4b9x3CXHs/+VyXO1/C9mi87ln9D/rzBOc8vO0n+l3lOTbfeYv2
8+m3E2q0+nuXqTvw3bv3fRhSZnyN7r1wrr79p8D3nhDufPcFvjtW1ere16r17fP8+27i/eOKeas1
6w3nXD4YvTf3fh/y7ufPfDb8O47//vXv9brvsoMKvP2U9fUeBCA77N+/X6+//robUDj/fLdzoaz1
6quv6oQTTtCoUaN0xBFH2FwAAIaWCcTX19eroqLC5oQr2LFjR7fpDNX8ouviiy92I/pmZn/oi8+P
Tj9BRSNP0jFunZGoD/e+qa07A/OfcrrOOa6nB5wH9V7HZm3vdJb7kTN09rFJyh58T7s2t2n38UU6
6+RjYntij/Phu29pa7v32tveExO31V9ekvd3QtFInXTMAe19s1U7Q6b74vP7Ov3ll1/WyJEjdfrp
p+uww3p6d7HMrzH842j+CApbV8/DkH3jMPuwdUeg3AmnaWRv+90e+x6PubPfO97erj3pLC+wvYVn
nKPYRX+Y9BiZ4YmnneUdx7e2ur/yi5+e6tA8REn3+ASPTdg11tvweOccPPmoD7z9ZfLtuX8gZL9E
jo+/fyPLKdTpZx+n2KMRuOb8cj1dey4zz9tq2+OUd4/v4dHx4HY4w1NOP9s9RonH7xSdcc5xOvy9
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

------MultipartBoundary--ZeJbom7ua2thyClsILZ3bxA8NwD3gXWgKq2ZLWICWB----
Content-Type: image/png
Content-Transfer-Encoding: base64
Content-Location: https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-DB0201EN-SkillsNetwork/labs/MySQL/week6/images/1.2.png

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
UrzIPNPHjFApJ/XSKOnnb96rqVcOyZZFG2OXr1olx9/ttHn7Fulu23tWm4CqDVzaIG7M+jeMlV9H
ltvgprfcC/zm+9qbeT+z63GKM3/eKOd9o2ZH6vHbv9EGmH0l0N5j6u5L88Jb7k6LV49Is31svb60
Nj8E+JPcPGpW/PLmurCWtG7stQ8sz2C9RfNazn/rS6sEy49Wfd6oITJqyOuyXusTnXMvsDzYviLW
06cB8f8nrw39P/nqq69Mef9+kd9dEgiMr1sun8s18n+2jVduL8ePIchkfx7xevD7LlB+PXGT2958
zz0n+o3rfX+ZZd76dD36HRZcP/WYelLzR8vdj78vzYY+Ko8+Gi1DW7wvj989uhzeBCymjVNk9AfF
DR83kwvufFTu7NfM1kugRJ+LY0Hw+ioPdQAAAACZFT9SPMfmLXQm5lV5qZdUCT+v+zlXyhXygAzs
2Ulemavzo8vzFi+Vz+evk3W2brx1vXx/12/cf8QUrZfXh7wvD44cK1u85fOek7Mu+qU0emN9tE39
X8rgu8fJFl3+vUvlYXlfDh2w7Z3JgkV/cl58IIf2u/Uc2SSHN4hc8Z1TbF3nR9vr8kl395EHz/Sl
fFn9ulzx3BC5771Nse0d0VcO836d2rnFrXtK+/7nfhDX3zFKuv50655Ey49SvXUT5z9F+2X11+65
tzawPNX7K0I9bXM+lNc02P2Lk+0MkcaD75ff9PlcfvcPPblcm1ctF+nTQVrZ+jEhg/15xOuNG0oj
5+XD0+x3UaBM/nknt/33HnHqj8hl5n0NzA2yRs3r2/UVyKSRv5SPmzRI/Xlmmr31ZObPmS9y8lAZ
2s3OsLpdM1S6yXx5r5SjpYGKJnh9lYs6AAAAgIwKHyluy2Hf66NZL42w9aVTX1PnCnlTA8rOOl4c
mitn2dGNZ3mju/3tzSc9LF/c110+m5PnlCpyye0Pi4z/WJbpyG8d/fj2n0Qe+kL+OahKtM3jzvon
/VI+nuu0WXWctBrirOWLWXYbZsnyR66QK5x589ZvdD8v/2uZ+PYVctl3Grp17/Nt0eWzJl0hr1/T
1X6GU3L6yGXOOj7etTXS3mXfb2vOgvj1pVn3C1ueTt146HV53dnWFzU1jX+5u9Rso6nPfdY5Hs/K
XK+uJd8dlfqK9mWk/jP5YO5YuU+Pmz1+9010+tJZpvPM8dQ25hjZz7MftWriz+xyLc/KPG95pMyS
v0WWO8U5Lwriljvrnqjbqm1+Ju/bz/GKf33mFwC+9el+uMvdkbMDH3I26q3r5XS7LPh+bfe+0+6V
idH9/ZuvL6L76xR7Dpv3m750+yCyPjvPv73uLxS8czP6a4T47dUyy6R6iXy+LbHbW/x62nrcLl99
dbtEQ+KqsXTItS+ttSs+lzP7neUsKRujRo2SHTt22Fo8XaZtkvH3R2n788jX3W0+sN1+FwXKf/O2
um1XrXLqq2SJfZ/LW189aV3DnVP67anY9cQ2yoZ8+zJONxn6aPxoaZPeI5Jm5XGZEhIzj23jlJhU
H25qktGToylboilG3BQp0feGjVQPtHktyVh2OwpeP3v+6GBbdzsi6wnZxpj0Kbou/+cmS1+S5HOT
903UPH+7NFKlmJQqvvWWJM0M0pPp6zMTdQAAAACZlSCnuDsmJScyNiV8WnbLSyvV+kOmm9bKlzmX
y5v2HyTr39DwuGPSL+XSnp3kf83Ia6+9Y0gbqbN4k60Uyvydh5xpJaltIm6FcvhdkSvaNZH/5m1z
6vq+bbKgihuwfmKRJjFuKH0udT7jm+2yRZdv2C6Lhlwhdzjz3p04z4wm35I3UcY5875Tp9CphWx/
t6Hyr6IxckkNZzs2jJP/dbbz7NYdZOgYZ1mlqs5/fNvriO/f2PUl7R/zX68eFFwePo1bfrClXPLY
63LFu7+U54L9a9h68wbOfxpIG//77ajUls399Q/koaGF8rA9hpoL/uPhfeTsi/3znDYX/8UGZbz1
PSA/mz7UTVVi2jwpP+2peca95XNkdM8fyIsPRUfkf3Gmnhf+9TSUlvr5wxvIF6bNRLmjm/d+d+ru
n47u7yQ/fe5h284p0x6WF4d2ktHzdHknuWOiu+1i06c89T3/+91XmvKlTX2RF4d/LDesdtfztLab
95yzv/G/ULj07nGyVd/3vcvkYWc7D+uvEez65i960vmvzvPWXyBF+foLBc0r4v4a4SH/rxHM9t4q
kzZ47S+Sp7zPN8KnxT4/SmWufDha5Mz23rhwt/75QxeVST5xDXZrufnmm0MD4zpPl3ntkkvUP7HT
o7/ck2i5rc/7i5wdc325csx11lVufMupPNTfaeO7vrzvN6+8ONudb+TIlvdudeaNM9dW2HL3v85U
rw/nWpj0om1nfrnjLl/gzbPFvR5VgbveF72TRee717H/c3LMNvquC7OfvnV6vxKy7be89/OYzy9+
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
CwAAAKCiiguK79ixw746cnTkydvjF8qHny21c0rv/LM6yvcHdmF0EVBKdevWNdOy+C7IFtqn9GfZ
oK/LDn19dFT0fue8Kj/0WAAAAAAVVVxQvLAwc6O3E6ldu7aM++Ab+WTaCjsn3L79B+Xw4SKpVClH
qlerYueGO+eM9jLowhNl165ddg6Akqhfv76ZlsV3QbbQPqU/ywZ9XXbo66Ojovc751X5occCAAAA
qKjiguJbt26NpFE4UlPNJX7wUI4cPJhjPzXca2/Nlm+XbZYTjm8s11zZ084NV6VKkVSpXGTyiqe7
HUyZMo2fNmzY0FxT+l0Q9I+pX8sTb31ia/Ea1Kkpzw67TE5o1SSmrX++Z8Q/PpK3P5tvXrdv3lBe
uP370qhuzZj5QWd2bS8jbhggNVLcJPPztuP7Z3WTe//nPPl2bYHcOvId2bZzj20RFbadmaB9Gtaf
Ktn+qpG3Xirf7dzW1pLz1uXvT4+3zOsHv737D8q9L02Uzxe4NyrD2mzZsUdufuptWbHB3Y9gm2C/
/urKc+R/+p6StL89XttMSKevw/avuOjrsjuvPcnWmeyYBvsl+NnBYxJGvxvuvqqvPPrm1DLr30SS
9bsn+F0d7J/gORbGe89/F62SYc++a+b5+86/jmT9X1zp7F+6gudMsuPj389EfxZ4/VqcP4v825Do
fan+bPW223+uhvW5t55M/VmmxwIAAACoqCrZacThw4dNYDmdadWqVU1Jt7031bzflSsdllo1JbTU
rpUjTZvUlmr2Hw061brOD2uvRden603n8/1Tbx/Sbc+U6dGcvvXWW/I///M/8sMf/rBY05kzZ6a1
fp169HWwVK9e3S4Np4F1bRNsq0GkeSs2RtZTULhL5izLt0ud67dyZfOsAV1WrVo1OzeeBgKG/997
snvv/si6UhVvO3S9Xl23M4xu59WP/F2+cD4nuJ7SFBU2X0uy/VVef6ZTvHVpkGrKnKWhy7x+8Je1
W3bIwlUbzXKlx0aPkb+NHh//w5GDbfT4+oOF/vMgUX97irOPqYoKm68lWR8Ut9DXpTuvNfhY3Oss
2To16Hjbc2NDvxuC/fXZgpUxy73vn2S0X2vWrFmm/ZuoqLD5Xvn7R3PiAqzaP4/8/cNIm+A5FsY7
f8/o1lH69uhk5o35dH6kj/86cbo5/zu2bCK/vKpfZN2lLSpsfnGL7m/wJor2i/ZPWHs9LzzBP7O8
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
//SraSjvSWxclo1/3vFzvHDD5ToHiS7u3qkez7z9N3SMaotOI0bj4n7j1qcXi4pQebESLW+IR1TX
OLXs4EdZKD5bjNjJTyF6oDdHLBEREVF4YFCciIiIiJqqJhUU//20wZg36cdqOm7wWJSjGb5cl4Ez
x430KU01IC4FC4p7XX114wyK52Uux+zPxcTdifh6Uo86jW62O787F2XvrESzU8fQtc8wtSwqViWw
wblvilH05Sdq+mLb1ug8YQYD4kRERBSWGBQnIiIioqaqSQXFU6YOQVSk8XPZu26IQWy7lugwYBS6
DHtSLWvKggXFZ8407p5ZXa7w70d1P6n38/0k3vHnyHV3+cQxnNv+KUq3G9m5L5eeRNXFS8AP2qP9
0OFqWbvBdyGqkxEsJyIiIgo3DIoTERERUVMVLN0lUT3z4PD+/TWO/PYc3q8u1Hzv+YiJiIiIiIiI
iIioSWhSI8XDmf1Gm3YNb6Q4ERERETVkHClORERERE0Vg+JERERERBSAQXEiIiIiaqqYPoWIiIiI
iIiIiIiIwgaD4kREREREREREREQUNhgUJyIiIiIiIiIiIqKwwaA4EREREREREREREYWNgBttEhER
ERERERERERE1VRwpTkRERERERERERERhg0FxIiIiIiIiIiIiIgobDIoTERERERERERERUdhgUJyI
iIiIiIiIiIiIwgaD4kREREREREREREQUNhgUJyIiIiIiIiIiIqKwwaA4EREREREREREREYUNBsWJ
iIiIiIiIiIiIKGxEVAl6+oqsWbMGW7duxblz5/SS4Fq3bo2hQ4fivvvu00uIiIiIiIiIiIiIiOpf
SILiMiC+bds2jBs3Du3bt9dLgystLUV2djaGDBnyvQXGqyovqMf92dPhOXgWlZcrENPlkloWn7gc
za7qqKYbC9mW1ZHHJ5iZM7djyZLBei48XPZ48O3WrSj7fLOeP4FK8S8yui3a3Xa7WhZ98zBEdb5G
TRMREREREREREVHTEJKg+DPPPIPExEQMGjRIL6lZbm4usrKy8PTTT+sl362v33xAPVZVXIsedzyK
iMhI7Mr8nVrWptMAJExYqKYtjq/FL57aio16NlAcVq+cjIF6LoB+fa+585HSX8x/sQLxabC8ZkfG
YhSOm40JnfQCl7Zv366nrGbOnKkegwXFZUDcrObg+A6kPpyFZXpOGj5lBv56T6yea/jKd+6E5623
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
mjXYunUrzp07p5cEJ0eIy4D4fffVbeRtMC/O7oFH/+0tNd0q6irkvDwN0V0r0OXGO9SyMwVFOH/k
GG79961qvikZMmSInjIsWbIES5fqGaG+0qrUnUz74T44e/yDxTUHjatx8fhR7En9P2q6/cXL6DBi
OMqzslBZYeQJr6qoQAUigIpKMddcLYsel4Ti9Wtw9LIHNy9Yrpa1ju2mHomIiIiIiIiIiKhxCllQ
vCGQQfEZv/27mj6z+WVcPrkPX+/4EiUXItSy1p0748f/GSz5cuO2fbt5eJGfNzDeuIPiMtf2Unxw
2xWMbhZOb/lMPe79y59wdYs26DRiNC7uN259erGoCJUXK9HyhnhEdTVGpR/8KAsHvz2I/r95DrG3
j1HLiIiIiIiIiIiIqHFrUkHxSXdfjXmTfqym4waPRTma4ct1GThz3Lg1f1MNiEvBguJegwc3zqD4
joxnMWGdmBiViEJTTu4rcXLLP7Fv2WLAcwRd+wxTy6Jir1WP574pRtGXn6jpivbt0PfxFAbEiYiI
iIiIiIiImpAmFRR/aERHREUaadLvuiEGse1aouttSfjhT55Ty5qyYEHxmTONu2du27ZNPZLh/NFv
cOzjD/DNJ2vU/IWTx1F18RKadeyAa4cbF1a6/Og+tO7SXU0TERERERERERFR0xCSG20SERERERER
ERERETUGTWqkeDiz32jTjiPFiYiIiIiIiIiIiBgUJyIiIiIiIiIiIqIwwvQpRERERERERERERBQ2
GBQnIiIiIiIiIiIiorDBoDgRERERERERERERhQ0GxYmIiIiIiIiIiIgobATcaHP//v16ioiIiIiI
wlXPnj31FBERERFR08KR4kREREREREREREQUNhgUJyIiIiIiIiIiIqKwwaA4EREREREREREREYUN
BsWJiIiIiIiIiIiIKGwwKE5EREREREREREREYYNBcSIiIiIiIiIiIiIKGwyKExEREREREREREVHY
YFCciIiIiIiIiIiIiMIGg+JEREREREREREREFDYiqgQ9rezfv19P1U5ubi527dqF8vJyvSS4q666
CjfddBMGDRqkl3wPqi6qh8s7n8Gpb8pRebkCbTsZ295myH8CUT9Q043F+PHj9ZSzt99+W08FSk09
gZSUq/VcmDh9GhH5+ajYvUvNVp06jUrxr6rNVYj84QC1LDKhPyI7hFm7EBEREWk9e/bUU0RERERE
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
1zi17OBHWTj47UH0/81ziL19jFpG1CSokYXBRpETERERERERETVtTSooPunuqzFv0o/VdNzgsShH
M3y5LgNnjhvpU5pqQFwKFhT3Gjy4cQbFfalArjCdjNnJLf/EvmWLAc8RdO0zTC2Lir1WPZ77phhF
X36ipivat0Pfx1MYEKemw5emoTbpH4iIiIiIiIiImpYmFRR/aERHREUa9w6964YYxLZria63JeGH
P3lOLWvKggXFZ8407p5ZY67wMHP+6Dc49vEH+OaTNWr+wsnjqLp4Cc06dsC1w40LK11+dB9ad+mu
pomIiIiIiIiIiKhpMCLIRERERERERERERERhoEmNFA9n9htt2nGkOBERERERERERERGD4kRERERE
REREREQURpg+hYiIiIiIiIiIiIjCBoPiRERERERERERERBQ2GBQnIiIiIiIiIiIiorDBoDgRERER
ERERERERhY2AG23u379fTxERERERUbjq2bOnniIiIiIialo4UpyIiIiIiIiIiIiIwgaD4kRERERE
REREREQUNhgUJyIiIiIiIiIiIqKwwaA4EREREREREREREYUNBsWJiIiIiIiIiIiIKGwwKE5ERERE
REREREREYYNBcSIiIiIiIiIiIiIKGwyKExEREREREREREVHYiKgS9LSyf/9+PVU7ubm52LVrF8rL
y/WS4K666ircdNNNGDRokF5CREREREQNSc+ePfUUEREREVHTEpKguAyI7969G+PGjUP79u310uBK
S0uRnZ2Nfv36fX+B8aqL6uHyzmdw6ptyVF6uQNtORkC/zZD/BKJ+oKYbi/Hjx+spZ2+//baeCpSa
egIpKVfruTBx+jQi8vNRsXuXmq06dRqV4l9Vm6sQ+cMBallkQn9EdgizdiEiIiLSGBQnIiIioqYq
JEHx1157DUlJSbUKcMtAemZmJh577DG95Lt18fNfq8eqimvR445HEREZiV2Zv1PLItr8Czr+yJi2
OLUF8/5UgM/1bKAuWPzcaCTouQD69d2nTsHMeDFfmINRGbC8Ji/zv3Hgzp9ibC1j8idOnNBTVjNn
zlSPwYLiMiBuVnNwfA+WzNuM1XpOumXcODw3rIOea/givv4aVR99hOhusWgzwAiAR8REA+fP49LR
b3By3Tq1rPTSJUSN/Qmibvyhmq/eSax9JRsLD+pZs2598NbjN6P2LWS0Nbz9xaWTm/8bqzv9tFav
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
Du/fX2PeXM/h/epCTSgD4kREoVJWUizOUQyIExERERERETUmTWqkeDiz32jTruGNFCciIiKihowj
xYmIiIioqWJQnIiIiIiIAjAoTkRERERNFdOnEBEREREREREREVHYYFCciIiIiIiIiIiIiMIGg+JE
REREREREREREFDYYFCciIiIiIiIiIiKisBFwo00iIiIiIiIiIiIioqaKI8WJiIiIiIiIiIiIKGww
KE5EREREREREREREYYNBcSIiIiIiIiIiIiIKGwyKExEREREREREREVHYYFCciIiIiIiIiIiIiMIG
g+JEREREREREREREFDYYFCciIiIiIiIiIiKisMGgOBERERERERERERGFjYgqQU9fkTVr1mDr1q04
d+6cXhJc69atMXToUNx33316CRERERERERERERFR/QtJUFwGxLdt24Zx48ahffv2emlwpaWlyM7O
xpAhQ763wHhV5QX1uD97OjwHz6LycgViulxSy+ITl6PZVR3VdGMh27I68vgEM3PmdixZMljPhYfL
Hg++3boVZZ9v1vMnUCn+RUa3RbvbblfLom8ehqjO16hpIiIiIiIiIiIiahpCEhR/5plnkJiYiEGD
BuklNcvNzUVWVhaefvppveS79fWbD6jHqopr0eOORxERGYldmb9Ty9p0GoCECQvVtMXxtfjFU1ux
Uc8GisPqlZMxUM8F0K/vNXc+UvqL+S9WID4NltfsyFiMwnGzMaGTXuDS9u3b9ZTVzJkz1WOwoLgM
iJvVHBzfgdSHs7BMz0nDp8zAX++J1XMNX/nOnfC89RbaXNsJbQYMUMsiYqKB8+dx6eg3OLlunVp2
trISXR75OWKGDlPz1SvB6qeXIqVQz5rFD8XmZ8ailodUMNoa3v7i0vEPFuOv186u1Wvc2rl4NOaI
TQomYdYKLLrfoS8czcSTjxzA1JxkGC1usj0do+dm6hkgKS0HyQHdcCfSR8+Br1biAuTMtq1J/Y10
5OnZoNvSUHnboW8yVixOQui2vASZsycjPd6hzcKZau9CJL++CEm89lWv5Hkjo7vz+9F6TknCAodz
hJs67s4jTvT7I1/PBnn/udoGR9Wdu2x/287pPFcdWxvYuW+TxqvknScx+SXvp4Cd7bi56TOu+pWL
zydXdRyEbBuJiIiIiMguJDnFZcoUNyPEzWR9N6lWGqJpc+ejcKVTqSYg7qT/ZOtrvliBCUY8tkGS
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
3GdCmliPgVx7Aro+BXLtaWoau3O3ptWWseUYFCciIiKijqrVguJtwa9njMHzD90jhxPGTEY1QrB/
43JUFR2V484pIN7G+QuKu/Xs2UpB8VbjDoo/gP93eVMpbaXYsiwd/3fjT/Ha8IYmAhxNq9m3C5V/
fw8hZacwYMR4OS48Xubq4+zxAuTu/1IO10VHoc/UJwMIiBMRERF1PAyKExEREVFH1aGC4nMfG4vw
YD3V6ubhcYjvFoEeoyei3/hn5biOzF9Q/Kmn9N4zP/roI/mz7QgsKJ65ZgVmfaMN3J6C7x8a3KLs
ZjsNJadw9tuvUPGtXoikoaIUrrp6oHssYsdNkOO6jbkZ4b31YDkRERFRZ8OgOBERERF1VP6eOSY6
zy7HL997AW9N7K1e27v5mReQo02XM21YqwXEiYiIiIiIiIiIqPPqUJninZm1o02rtpcpTkRERERt
GTPFiYiIiKijYlCciIiIiIh8MChORERERB0Vy6cQERERERERERERUafBoDgRERERERERERERdRoM
ihMRERERERERERFRp8GgOBERERERERERERF1GgyKExEREREREREREVGnEeTSqGEiIiIiIiIiIiIi
og6NmeJERERERERERERE1GkwKE5EREREREREREREnQaD4kRERERERERERETUaTAoTkRERERERERE
RESdBoPiRERERERERERERNRpMChORERERERERERERJ0Gg+JERERERERERERE1GkwKE5ERERERERE
REREnQaD4kRERERERERERETUaTAoTkRERERERERERESdBoPiRERERERERERERNRpMChORERERERE
RERERJ0Gg+JERERERERERERE1GkwKE5EREREREREREREnQaD4kRERERERERERETUaTAoTkRERERE
RERERESdBoPiRERERERERERERNRpMChORERERERERERERJ0Gg+JERERERERERERE1GlckKD4X//6
V9mIiIiIiIiIiIiIiC6m8xoUd7lc+PTTT7FkyRLZxLAYR0RERERERERERER0MQS5zlOUurq6GgcP
HsQDDzyA7OxsOW7EiBH44IMPMGzYMERGRspx7dm6deuwY8cOnD17Vo3xLyoqCuPGjcPdd9+txhAR
ERERERERERHRhXbeguLbtm3DLbfcgoaGBk92eFBQEEJDQ/HFF19g/Pjxclx7JQLiO3fuxJQpUxAb
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
JID/D6lrPsMP6D2cAAAAAElFTkSuQmCC

------MultipartBoundary--ZeJbom7ua2thyClsILZ3bxA8NwD3gXWgKq2ZLWICWB----
Content-Type: image/png
Content-Transfer-Encoding: base64
Content-Location: https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-DB0201EN-SkillsNetwork/labs/MySQL/week6/images/2.1.png

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
7Sqx17wE188r5XMf87nuNqczkb4skWyeONvb91M1rpTm/flUDdufeqxvv75fV//hKv3whXsCxxpI
di/ORPqyPJK3icTWYguum3dy1wyu603Pc56z6/WoGn/qtavtJ58/vb/7JTOl90PPfu+br+nqrzl/
yV4eePa9Vc3KqXmjks3qTKQte/O18zXqOunpPanH5iW7nrOF9GXxk7sFO8xXcP28kruWI2qZk3yJ
eXbamUjOc5PzfeFG+p7Rjte8eb7UfPbZnu3c69a/1aO/Tl1mfqW24V+k6/9oks655vOa52yvpSPq
mptkd5DhuvuilhWa/O0VIrh+XsldyxGe73yf7f/kHN13XasWr9mWmO9LyZsh+aKW+ckXtSxb8uW7
rC/J32a+guvml3q0tulR58vrK7r5nP3OZyCwzL0/n9cPH3le/6vCznP34kis73yf/fQb+mzFdYn0
QNpnwkm//seUPJ+t+IbW7ksud7fx3Z9q7V12+XeTz0Oc5B1S/tfNCK6fX3JXc0QtC6dteiDl/P9R
ncHl5vrc5Zz/d+1yZ3y/XeeBX4fWda9N6rz0a+7cV/9a+ilxTc26f6R7nnYOffmfOctCxxIjuWdt
h/kIrptv2t/RprbrGjT3k69q/+s2uGmT+U4e9rnJun7elfpY4LkyqdO/pm4KPnf5XYfU7TjJvUf+
cu96Lwy9+911bD73Gf/THzg7e1r3/FFq3vC2Iz9DaSn9Hqet5/wdbWFgeWoeu37aZy39XDJfw2RK
yeOc8+/cO53rXqeeg9mnu52UZzV8XtHHnf17yFvngZ8mr4f/uQrfM++7KvocsyX/XAEcv8Kf69yp
R+u+/of6oqmV4gZJ/lkzzt6rvXudtP+NZL7un+mua2dqz3wbcFk+TWeaPE7a/0Zwe/klAACGmiHV
CG7UyzNnGj9Z88w/2G76A/1V6B8Kbx94Vd3dPTroz7PFI+5YIF9kipM3Th6b9r+6Q7pusiadezBi
+dv60JiPa9irB1IDCjZ5u0mfH5n2bdEzrbfrzi99Sbffe4qW/OhZvR0sNIqZ+iJqeznTcXIfew/s
dY7ydt0wJvpeHbzm47oqeKyB5O0mfX4hqVBR24qT/GN3Jrx53gwdu/hLuu/e6/T0//m21gX/Qe4u
TeYfWXmDrtcPNKvyD9IKQQ72dKs7+Own1rbT2VLWvC/rxael66+4JGKZk7wVo5flkfoians5k3fk
7jB9uXtK3lJ/XnJOIJ9Ne36vX+o6jb7ETtuczkRqPicdPPdSjXaWvvRquEBmo3Nnr9OUz31Qbx+8
SjfMk/79qS2BwrdQSuwivMyd7S5MX9a31BdR28uZkmeSvuzg2brsY87Crj3Ja2RzOxOpeaNSnLxx
8qQldw13vcjldpkzkb6sj6lQUdvKnV7T7g3SvD/8hA5EvRudZ/iqT3ar56Cdds/cjjtp/0+/qS/8
n9OTTbs93aBdfxF6b5lmLv7ilZTm3344b5OW3JwsxD5z2OnSqr/TM1Nts061n0uuHzP1RdT2cib3
WrhXI3q5n/b9TH9V+T+0MtCU3A/nPap5lYFC/LPOkDb9nZYMs3ncJkOGuc3arfyLlfqkvXZus5mr
/oc+V5k6b+VffDPwzulx22hfMibQdJ1zX6531vPuy+f0NynN23lNeqYcc4xUqKht5U49evapZ3T9
H1XoHP9ZDKW3z5uq5V+bpvMuS87rfPAPnFMMNDP6yFXOc+e/d+NfB3c7O4PN/a3SPOd+feFBv2D/
TJlH+PRhZ6asN8y0k3f6MJ3pjI+ctdzZ/+3ODK8pRNPci3evwsd4u3M/0/9ukJoi7rG7XuA5MM/d
zX+nqwPN06U+KxfrpqnmedqYGkwyf2/edJ2+9HlzfLmuoZfCeX41tU21y927bW54Il9qsudwun9d
n9aXnr7Z3AqZC+fl8T4DZ5wVXM+71sk8cb6HvHVW/p82Zx9enr+p/JymOu/ntqdT38+dv3rUuUVf
0E2B5yhuAnB8i/pcZ08j9af/4nznjf4njfrY1U66Q//SFZHvsho97HzHXfmPJo+T/rRJO8J5CkgA
AAw1x39Q5Y2r9Q3bTn/bvTO8KqZu+qeIX+CZvTytRTf5eVLTX/0sWFho8joS01HJy7LiT6O3NyHx
j89e9XQ94+Q8qvfeCm/DS2+9cTBRXTYtebvJcSw2XfYn+v4Lf6WrDxzQOV/6J/3+7gnR+XKkvoja
Xs6U932Md939vGYkdRvB5GWJs739O7ucnMd0JNOvbJz7GBVQcZO3m3j3MUcqVNS2YqW09e2MYwc0
7Etfce5bq5Z8+2eJf6j7K/j53zKFP6aQy5m36n8Eru3Xkuskk1mz75/Tzgfv0Pd1u+6cdm7aMud/
Kzw//9QXUdvLnRIrh+Z7yVsW3LY3y4wE85lfxC6b2+gGe6/7iDcvfN9S0lsXujV/SkpSC9E6Nz/s
buPa895ypg9qzPWmCbDF+tfIAjJv+2ZH6cvswuW3R9736O+CeKkvoraXOyVWDs036S1dVGYu5Clu
waOZ5173p/+3qiLP+5ta151cP+s9simf7aWs5244etuFbjNOKlTUtnKm7pf0e2fdY4ejfuBgkvMd
nvL97u3LjJjPzL/eu0nX39ug6Wfv0759Tjr7S14TlfeuTjyfnZv/VZr358k8TrrKfC60W3v86+Ru
9HZ9deoZXp79mY4nc+qLqO3lTomVQ/NTU+eP/86tYfGruz6ePP+7zPv9X9X4M//722zI1N61edwm
Q8w8x7z/oRn22p352cnue+P6e/9PaN4m7T5g99ntFYrfNyu5v31nV2iK8zFr22v6HDmonn2H5DZU
dOw9Z3n0Dx9ypUJFbSt3ek0vbXBWPvpe5r8bvnVA3fud6+b/vbL7Z2pc5Vy+R/5KV/nX4eq/cpvY
XLXSvGvjXodtajXb+Ysv6Ux/O/s+7gbMtXNv8j3vSl3XPtju+FsHurXvPa+5liOHvOZeen+9WkvM
vXo60zGmbi+ZXtPuTc5zUPZRezzeer9/Yblus8GA/b/2avbcfrVd7qTUZ+UtfdDU7tHDag28n/b/
+pd62n+H5byGzjoRec6cusQLVjmSxxxK/rk3+Nf1DN283Pt7b/J7192EmUiu589M5In3PeSa9xe6
2ebpcf5+6r2ff6lnE9/Xzr3+galpWqkPZvj3SbYE4PhlOtcNN7GVOx3S/r27dcbUf/YCui98VXv/
5POq/AMn/dN/JvMd2q+9u093vuNs4Hd+t6aaPE76Tmdwe/GTOVZzzAAADCVDKqgSpy3N9Ok3nJf7
x/UN98XuJPdXcca/6v+59g818R+TBeJe2+jeL+a8vwikpodne79Sc5O7DfNneH+BaZsjYwfntcmA
xqnm7wDu5rJsL8O0t6LzZ5z8b72mfXv36w1n+lBPalXcuPszqS+C24yf4t9H/4pkvu4TU/J6ue10
VLI54mxvmP+JCa4fM3l7KWzdcCpU1LbiJPfY3YGd581x/3zrtU/oG+Z+tf297vuZV2BmFyXzm+fS
+Uf/Q/aaep32O3719/qic3/v+lkgUOIuyPY5HRnK+7QWfcF5RsxzEkj/j3NMPzQBxtdMYb/Nn0ju
ivYQw8vyS30Rtb2cyVvTTenL7SIz8Oe5U1HX6C+1yvxa+f9OTRSmuNxt+NsLpiPud6i32M7r/pke
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
Tii5PkznhgWm7wZlGLZzl61W6fxubnts263Sp6Xye1sgLPE9T3I68buW30/3yen/eL9c9PoD8nza
+ufdj7j1YEvSrpP3V7r14LrVP/2qHH/Nz2S9+54nOC1fV11lq7ca56axZYfaZnb7+b+n/enjSt93
d8nHH5nByWG2Vw8w/XYeN0h56Ngzx4cuwaKOlVHqAiIQKJh9jXnyWY+nz+/ecnV2D1D82QT0dsn2
DTpAcK50dp9v2632jT+/In+yM5D4rX19bHs7s996Wt70ggrm2I23DvdFPlyzywTLzS8lhgW7PpEP
V+0R0+Ri4nv2/fqNui0gbxyvlKgbJ1Y65K15bxrJzi7/6/LH+cvkE3W94D8X5dI1JQ0C0Pr69esn
e/akPlxVrP16XvU8AwBQTLKWVLGns+ani3Pu32+r3/KeSojzesEN6qZz2X/IF596L+XzVb/4nvzp
azfItH5uuPutxsbU6aS8unHVgPTjqc5K87n/dVc3mTpTzetzt8mFT9m6nL3PVz11tTy0dLI8OHOK
ubELf9/jtakS/rzQr3o75Fu8Vn9PF8+N+1vea3I7BteNfl3ttuOX+nnD3Y+prRSeTsqrN2bGbe5G
ijO9vdttg7tL1bzevUh2+D7fuehe+fpz+unO2+WUnanf94SH5/qab/HnfI8x/ZrgDU8M84+3S7ac
fHuiihDDDB8p02+7TuQXt8mdKXXo7pQFP50tF/3wK3Kat++7r6oRfOOleU2MGhy+c8sJcqdp5+U/
5JFFuyK+n1ym4PDcXpt6rOS1PfadYqrvePZr98qL2/yfvydPXH2/OVa+2Nv3BJj7PTUgenq+18S4
oeE7Fup9O5hGrX7xAVki18klp0as373d5QJdxcrSZbJiu294xvWuhtlPQsOb9tqU6gL09/JJz9Km
O9sWyp23/rfa32fKtN77EsPTrffIVzOiXlnpx8tpeonXLOvffaZHjPw8z9eWT8/2yfZTdDq1VB66
+l5Z4N8/3fbRpUzu9PZr93vm835Xyg/dsZf8njrubp2ntulNcoHpH2Wqbfrpf/538vyw6mn5uomp
2GCo/p6V//pslf1adVam8fbJaToY8Nr9gfP56qduk9kqvfjG1N52PDel4Pe9ocHhbkhyvMQw2z9S
lxxYcp/85A1vOuq88qhOn5SPPnbbwaxtxTedHF5bfj9V57GeV8hP1XnsuVsvVdeNoWvc1U/LhZ/5
J/m/ap3ePM0G0feerqvhfE3uu/ppU7WVGW/7Inn44WXytdu+IiPN92OshxE60/5ZeeLnyfO13X7K
axuk0ow3QI7XwbNnl8gq970dCx+V+0zmv/4RNz3dq7n+fabNLTuP3ve84+NrN14pfVS/ftpZVxNT
UVFhXyu3m6DOE5+5VO70nc/3vveM/Oin6nufPUv1j5Sxan5e/fb/lTe86arj+ZGZurV/kfXlvvOU
d36aPU8tkw4qdDdBBTt/yXWYmD89HbMObXBHpwPm4Zpbk+t556LH3LIr3vdCr3b7vC7fcw976OGr
n7pBrWnNG2+YKUn3p8UrE+nHKt84Znqx0iGzFYzwfHjLv+S5ueZBifP91ws5vDbl+gdA69KlPQYO
HGjaVNm3L3k9ql+9Lt3x3xqf61Iqel71PFNSBQBQTErKKzbpc5U5YZl/ukdJDLNvZOWKt8xwT1lZ
mXtnzZs3T6ZNm2aeXKqrq0ucBOOor6+XtWvXSqdOnWT48OFuaEy9BsnwvjXy/PWT5R7vhsaZ/tz7
8q9n75eKrbvsgI3/LZ++ztwWpjFJ7vrF/XLFIPU207iT7pD/+eEXpP/BpXLflJnuKbhof/ejl+Qb
p7medPN64f3yl2e+JL32VErVPjfM58gb35dLv3u8PPfK/5JRblhz0k+86e04bty4nJ5Ca7HtmMt6
b47tKP1l6MgesvqhU+SqZ9wg46vy/Id3yen7K8SbVb9Cbcd8tk+Tto1i5v33n5HF/3a+dNYD3Dob
8+xLMj20MP1LlsmMz35XXr3wvuT4/YfKyB7vyQ9O/F8SWGVyrtz/6jPyDwP2SOV2t/PnfJx+LPcv
+I5M7mY/TVC/WfXkmXLVT8PbT9sksy++Xtbfv0BmntfJDctdqxwrSq/Bw6Xvmn+X4//hZ26I9ekf
LpFnp3ZLHitapnUUsvHnn5evuKeRg/S+/S05JZFGvS//9+I7ZPbX5sjqfxgiEbu79Gr8i/zvS+6T
hu/+Qu6/yHuyLNN6r5Ul/zZFvhs6/gP+7lH50w2nuJ54WmUbZdiHr///3pd/Oc23vyvp17vjpVXq
baZx/+bOX8hDX+iX0/SS3Po/4Rn50z+OcMOS8ptmdq2Rnmn9h46UHqseTjmG9Pa594zwdYMk0m19
7NUu+Lqc8y/JHVUfd89M6ei2aS8ZNPwT+Y+T/5eYdr2N6fL8krHyxOTvSuO//UJmXtgvNU3NUavs
1xnS/QBzPv+rPKjS+8Q6MNc5U6V7xVabXoTWqxWVPthh4v/N8HyotL7r/5uhtomrfkmZ/MASufXj
ySr9/4r87JVr5Di9Xbb+l5zyjzp72ncOiam19lN77qyWX0VcG+nqub49oVb2e+tU0fv1B4+qa5Pk
zmf26btO9q5LYqwHvf3Wz5Kx/2Cz8o1/+m/5ywlPqXXcKN/7xXfkIvWd/kO7ye++rubLW+3XzZW/
nPgTOWfhRb5zf0d587aL7Tgm/T5HHR995f1/98/jhfLgkqflS72ir50sfd31kTwcuobQx95PvnDQ
fC9lfuQC+eGSb8j6yWo/vO4n8qdrRrvhahHd+enVyTNlyb+fI42+a+/s6zBinAtmyoMn3yf3fOC7
7olgvvcfvmvHf7pfHlz3XblnrJfupqYfF35/idz2idqXG5Jpc/Z0yKbnL38u+hrHW355YLH8xzkN
4lv82PJNgwAUB51f8/HHH5uAxQknmMaditZHH30kvXv3luOPP146duzohgIA0Lp0oL8ogip6XN3Y
rX4i7ZRTTjHf0zPnvXrCw5Of95bBI/pK11C5m9qactmyy/f9/sfI6J6ZMlAb5NDuTbJtr5ruwGEy
qkeacRsOyZ5N26W612AZ2a9rxuI+tfs3ypad9r2d3z6p8+pNL83y9R48Qvp2rZea8s2yK+JzT3h4
vp+///77MmLECDnmmGOktDRrYaYE/3bUN1lRv5X5NWLdKHodbt7hG6/3EBmRbb27bZ9xm6v1vrti
m+zLZXq++R0wbLQEJ12bdhvp1z5DRtrtuHGLeUox/HncV51Jk+v2yXaMZXvtpfbBfp2P2PWlh7t9
vz5ivSS2j7d+E9MZIMeM6inBreE75rzxMh17hv5OhWzfp8Y327dDst8/H+q1/zGjzDZK3X79Zdjo
ntLh0G7ZtN1WZ+X/XtzXQhwr+WwP8xqxnhqilseMp9dRaD1HvHrrK5XatwP7rV1/nWprZOMWW01J
yvTcfiCH9kjFturA96LXe/TxH5Dp99K85nO8aE1KzzKkOynpmXpNv94d3zkiNd1J8rZ/LtNLzodb
//U1Ur55Z2D+9Gum3zVSjvd4r62RniVeI7ZTyvYxx48E9n+THvp21NTjzh0f7nNz/Oyul+6+48Gc
D1Samuncn+m1VfbrTOl+ymsovQ/vHxHrNTp9sNMR/3aJmA97fvVvkz1yoENftc/6zsuJ7R1x3sny
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
sk4WDn9T/Q2ZcpJc8/Qk6e96rV2y/MbfyZsLRMa++BW5/Gw3WNn1wv/I3JtrXF9Y8jfXPfacLHzE
Dk3qKee+9SWZeIzrjSk8reA8JefVLzzf2cWbTvblil7PKfNjtqeEtlGU9NsiKTzvwfWcbpvlso7M
cq/NsK+Ms/tj9PoR6f/kFXLNNPvNbPNjpiG+/TvB/tYHlyWnlU3V4vvlW3NT9nq5+M7Zcu1p6s2O
V+T+b86RdZ+9R2ZPH2c/lCp5Zea3ZM76i+We2dfKuES/+9gZe82/y3cvHeT6rNTfGyvX/p/vysUD
Xa9nzRyZ/sgrImOulX+/72IJTcX83hvnpk4/RabpeJ/5+cbz5jWxLhLc8krUvGXhpVOR6YoSkVb5
943Ysk0nMk1U/OlmrP0ph3QzbRodPj5DAvOUzVqZM/1BCW3VwHZdO3u6PPiH0H7n9oXEPhu1b4i3
v+fAO35cb1JyWnZ+7NCEwPFWWNHHfJrjMB1vuULHlVkWCc97Mn1IOZbC691w2zBlm9lPk3Kc57jM
PEnu29qvUOsnVvqbbptGTK/JkvPqF5XWZxR5XKTfnt72T/mdyOPUk5xey60fJ2L5AvMeufxKYjun
HgOG+57kur6zibs9wuOF5i9yPYeXIas0abiTOY1WEr8Xva8m+I6p6OPSL/t5pVDsvh5a9+F0Mt3+
4zuveNsieMzY5ZCc9/uI5Y86RyXmK/pcmX09OxmnE71dk8dymmNHc+uxoMd9eNsY6eYhfVrvba/w
cLs/RK/PTLw0MynzuoxcJ2bZ4pwLM00n2/byPo+YP7cf5JTeha8zHf/9XNR9WNR1dvheLPIaOuKa
+c0F4fyFzLKen7zjIeN1QPR6Du6XipnWG3Jelmun8Dz5p5NuX03Mk3dvlDiOQ/zLEWccLWK8lGUr
hMj5acZzYVOXy+yHlXJSVN6RLx9FIvMN7P3brsR+HeN+LvLesSn5aZlkP+/GOl+6/qDU9Cbe+Sk8
T77pRJ4LrGA6nn254iy7J15an9nb85bK1KWux3P+aKksG+F6rPB4d3/9fLn1JNcjm+Tx28vlIdfn
CY4TR7X8z6Nr5JZy1+uTmNYHq2T4f+6zAxN6yfzHzpAJrq+lxT3mM6WtiTQ0WzqupP5eRDqVxfYl
y+Ws3xxxfc7oQfLOHSfKYNerhce7/G9Pk/+a3Mf1RW+v4DjxRO6HSmJauz6Uf55ZpdIyv87yxH0T
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

------MultipartBoundary--ZeJbom7ua2thyClsILZ3bxA8NwD3gXWgKq2ZLWICWB----
Content-Type: image/png
Content-Transfer-Encoding: base64
Content-Location: https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-DB0201EN-SkillsNetwork/labs/MySQL/week6/images/3.2.png

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
JuL3o0E3d93G7B/Osdx2c32upFoe3cy7XM/yu8v1LLsux3XzdjlO6dKN7Tb2GgSg8cz5aN5wHTRo
kNq0aZPyvM2Hbtu2bfX555/r4IMPpmQIAKBZ5WXJEHNzrKiocItMmjeOgjdNP9HfPP1m+5v9YPaH
PzxdJr+Zbv/994/sx+C86W98v9muZvtmun9MXv8c8+flJ388/Zn15+JcYX80bX+254th8pvpuJ41
XT/Xs+z6c3lc+8OC86c/tj8Xx6l/DfGH+4l++ltjvzmes/39AyB39u7d6wYYgudpPiezrmadAQDY
VxRVVlYm/bVsflQvXrxYRx55ZNb1zy65d5SunGV7rAl/el3XnmB7jPd+p2Hfecz2hBj+E7141/nq
Yz67eT/XlNm/0oV93bGJyp7TNePu0Hzbm+jreuCN7+t42+dLWNfgco1U62nETxOjUn+7bpxWfDvu
+6dp8+bN+vjjj3XyySe7b5qkq9n2YybbvQn3Y8Vz1+vsWxfaPiMuX6P3Y7hs9k9j9437Xf/5pei6
+ttswh/11g+OdfMEufvx0/jv5h2X04KbTMMT903G52myvMF5hy07UcKxlkKLnCsNHtP2ex4W2C8N
baO44y/s/POEnwNR0e0buw0z2e6p82a6f4yW20fh2zzsOyTf7p6RN8/Wb8/v7X4OP7dipTu/VPmM
dPMG1zETLXE9iwi59ifsH3dfKsXx3/xa5LhOca/M9hhoNmb9nzhUvw25Z6XSosdpuvfOdDViO2Rj
yb3Xa8WlWa5rK5LOtbmQZHsNApAbtbW1evXVVzVmzBg7JAeW/EGnfle6f/53dZwdlKhSs3/0Fb06
9v90139kfs+fO3euTj/9dDcwAgBAczElQ+bMmaPx48fbIeH86hxLS0vdbmOUlJSkLhmyc+dOde7c
OdKffrdSz1zn/AGycpre/HiZPvPTvGla/Z1Ruua5ymj+4o7Ov6N1x7xAvmB66Ovqb/KZ/G7e9urk
dMKX63Q7dHJySJMeC5mXm/7b+XM1kH/js7rmi866dnw0Jt9Tx9yhs794vZ7ZaPON+O+Y8W/ePtoZ
eoWeCgxz1zVhvSqcP5hHadh1i9XpmNEaWnavhgXnm5A/vGv2g9kffn+6TH4znSkyn2zeybveuifb
j1c/W2HzOfk7prHd/fn6+7FDsuVmOD+3+77ucvbj2f86N2Zd37x9ja50ht/9ns2X7n6MzDe9rtm+
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
Ncz3PVz1NRq+ThraNGx4PJ49VyxIFdfqxte+2tifxbj2Vf05ZdN4ziuZan5WQ9eyZjiV7a/W9qvd
aDu1P6+h9YpjvcH3ckLB2ZjHPPp3enA/1dc9U32cY2/n7EuP13w9n8ZzXYfLvyPlqeq7Mq2qz23k
vmqf28TPCQAAAAC4NWY2DElvsj68K+59+liUuoamFx5cWqwwZE/VOqVH1xSvTMyWXQeHb+fJzbGs
eC2V3WDd8Xrsf75infuOFTd0l8YjT5aXH4z9G6q2N6FjWhNf3fV63L/h8fjOqbsjXn48vxZfHn48
4zXWeUVsrDin9Nj3xv0jApOOeKViO0c6knWqbuhuSc75hR8M3RQ/+vLr2bLJGOuYx7evyvMqH3PF
zeoa55VNtT6rc8l3r2t77N+1MXa+PJFgq8o4tlN57mfS9XaUj3lNPPH87tjStSu+Myz0OB/PPrc3
oqMznlhdLJoWQ9/p9Dhiw+44UxzXsP1sSF773rGh78trx+KVdNmgsbez7MGnsue11il1dcT6fLVx
Sf9O7+/cHkcGtxex7eGZCUSO7tsc21Z1Vhx7uq8aQcew85n4OQEAAAAAt86MhiFHX96b3UD86rTe
3J2CcwfjW51p8PJUPNJWLEut7pjmG9C5/Obw12PlG3tjZ3wlu4E6E/sZaWlsemBjRNfpOFksOfri
rjjQ0TksiFr/aB6afKtiRMC9D2yquCl+Ig69sSm2rsqeTLvJ7Gv9o52xJw4Phihnf3AoDsT2+FqN
gK1atm7Hunjknk2xpfOZSd9Yn+h2lqXrJcd8srxe2+b4WkfEzh1DN9zPvvTN2Na1PY5MMgScslXJ
tY9Dcag4xjSY2vrA3fmTm23w73QobFj24NeT7+rh2PbiFEKsUax/9Niw8Cz/vPbGoYmM0AEAAAAA
ZrUZDUOy8lAjfgF/62Q3sW9iOJOX1tkcL8T22BPPJPMTLIE0aSfiO7sPR3SsK24mn4hDnRFbVizP
ng1ZGitXRRzIAonzcfKNZFH7uqGb4unogAfWxcpk9sCp0+kbpsnU93Vvex5+LGtPb9gPD3RqOx+H
vnc49ty3JqIt2e+GoUBlYia+nSyISr4Dmyq+d3moUz7u/PPasuuhWzLS4OyZ15P/r4hND5RH6uTB
1Kb2ZLYiULtpzp0ecb3ysCiZeePU0OgVAAAAAIBxmtEwJB0ZcST7BXxeY/9GfSfK65SnifWoGHJg
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

------MultipartBoundary--ZeJbom7ua2thyClsILZ3bxA8NwD3gXWgKq2ZLWICWB----
Content-Type: text/html
Content-ID: <frame-65EB4390E2CE53ABFD5E9E4657537F37@mhtml.blink>
Content-Transfer-Encoding: quoted-printable

<html><head><meta http-equiv=3D"Content-Type" content=3D"text/html; charset=
=3DUTF-8"><link rel=3D"stylesheet" type=3D"text/css" href=3D"cid:css-f32224=
9f-f8e1-47e1-b129-5dde836d8e58@mhtml.blink" /></head><body></body></html>
------MultipartBoundary--ZeJbom7ua2thyClsILZ3bxA8NwD3gXWgKq2ZLWICWB----
Content-Type: text/css
Content-Transfer-Encoding: quoted-printable
Content-Location: cid:css-f322249f-f8e1-47e1-b129-5dde836d8e58@mhtml.blink

@charset "utf-8";

html body { border: 0px; margin: 0px; padding: 0px; }

html, body { overflow: hidden; }

.ita-kd-img { background-image: url("https://www.gstatic.com/inputtools/ima=
ges/ita_sprite8.png"); background-size: 850px 250px; }

@media (min-resolution: 144dpi), (-webkit-min-device-pixel-ratio: 1.5) {
  .ita-kd-img { background-image: url("https://www.gstatic.com/inputtools/i=
mages/ita_sprite8_2x.png"); }
}

@media screen and (-ms-high-contrast:white-on-black) {
  .ita-kd-img { background-image: url("https://www.gstatic.com/inputtools/i=
mages/ita_sprite_grey8.png"); }
  @media (min-resolution: 144dpi), (-webkit-min-device-pixel-ratio: 1.5) {
  .ita-kd-img { background-image: url("https://www.gstatic.com/inputtools/i=
mages/ita_sprite_grey8_2x.png"); }
}
}

.ita-ff-black-enabled .ita-kd-img { background-image: url("https://www.gsta=
tic.com/inputtools/images/ita_sprite_grey8.png"); }

@media (min-resolution: 144dpi), (-webkit-min-device-pixel-ratio: 1.5) {
  .ita-ff-black-enabled .ita-kd-img { background-image: url("https://www.gs=
tatic.com/inputtools/images/ita_sprite_grey8_2x.png"); }
}

.ita-ppe-can, .ita-ppe-ant, .ita-ppe-can, .ita-ppe-can-list, .ita-ppe-tbl, =
.ita-ppe-td, .ita-ppe-div, .ita-ppe-uds { font-size: inherit; text-align: i=
nherit; background-color: inherit; }

.ita-ppe-ant { color: rgb(169, 169, 169); font-size: 14px; }

.ita-ppe-box { position: absolute; display: block; background-color: white;=
 color: black; cursor: move; border: 1px solid rgb(205, 205, 205); padding:=
 6px; font-size: 16px; box-shadow: rgba(0, 0, 0, 0.2) 0px 4px 16px; z-index=
: 2147483644; text-align: justify; overflow: hidden; }

.ita-ppe-box.ita-ppe-box-mobile { box-shadow: 0px 0px; display: inline-bloc=
k; left: 0px; padding: 6px 0px; width: 100%; }

.ita-ppe-can { margin: 2px; padding: 4px; line-height: 16px; height: 18px; =
}

.ita-ppe-can-list { cursor: pointer; display: block; min-height: 1.5em; mar=
gin: 6px 0px 0px; padding: 0px; white-space: nowrap; }

.ita-ppe-box-mobile .ita-ppe-can-list { overflow-x: auto; max-width: 100%; =
margin: 6px 0px -100px; padding: 6px 0px 106px; }

.ita-ppe-cur { display: inline-block; width: 2px; height: 18px; background-=
color: rgb(84, 189, 240); overflow: hidden; text-decoration: blink; float: =
none; }

.ita-ppe-edit { height: 20px; line-height: 20px; font-size: 18px; text-alig=
n: inherit; background-color: inherit; padding: 0px 0px 6px; outline: none;=
 border: none; white-space: nowrap; font-family: Arial, sans-serif; cursor:=
 text; }

.ita-ppe-div { white-space: nowrap; }

.ita-ppe-box-mobile > .ita-ppe-div { font-size: 24px; overflow-x: hidden; }

.ita-ppe-logo { background-image: url("https://ssl.gstatic.com/inputtools/i=
mages/search_button_normal.png"); background-position: -197px 3px; width: 4=
8px; height: 20px; margin: 2px; padding: 0px; float: right; }

.ita-ppe-pgd, .ita-ppe-pgu { display: inline-block; margin: 6px -1px 0px 0p=
x; width: 22px; opacity: 0.55; border: 1px solid gray; height: 18px; border=
-radius: 2px; transition: all 0.218s ease 0s; background-color: rgb(245, 24=
5, 245); cursor: default; }

.ita-ppe-navi-box { padding-left: 6px; white-space: nowrap; }

.ita-ppe-pgd { background-position: -816px -66px; }

.ita-ppe-pgu { background-position: -616px -116px; }

.ita-ppe-tbl { width: 100%; }

.ita-ppe-tbl, .ita-ppe-td { border: none; padding: 0px; margin: 0px; }

.ita-ppe-uds { border-bottom: 2px solid; margin: 0px 1px; }

.ita-ppe-hlt { color: rgb(34, 34, 34); background-color: rgb(241, 241, 241)=
; }

.ita-ppe-hov { opacity: 0.9; }

.ita-ppe-dis { opacity: 0.333; }

.ita-ppe-dis-text { color: rgb(119, 119, 119); }

.ita-isv { position: absolute; border: 0px; margin: 0px; padding: 0px; back=
ground-repeat: repeat-x; }

.ita-isv-grey { color: grey; margin-top: 0px; }

.ita-isv-red { color: transparent; margin-top: -2px; background-image: url(=
"https://ssl.gstatic.com/inputtools/images/tilde.png"); }

@media screen and (-ms-high-contrast:white-on-black) {
  .ita-ppe-pgd, .ita-ppe-pgu { }
  .ita-ppe-hlt { font-weight: bold; border: 1px solid; }
}

.ita-ff-black-enabled .ita-ppe-pgd, .ita-ff-black-enabled .ita-ppe-pgu { }

.ita-ff-black-enabled .ita-ppe-hlt { font-weight: bold; border: 1px solid; =
}

.vk-box, .vk-btn, .vk-btn-n, .vk-cap, .vk-cap-i, .vk-t, .vk-t-btn { display=
: inline-block; user-select: none; }

.vk-box { height: auto; padding: 10px; background-color: white; border: 1px=
 solid rgba(0, 0, 0, 0.3); z-index: 2147483644; font-family: arial, sans-se=
rif; font-size: 14px; position: fixed; box-shadow: rgba(0, 0, 0, 0.2) 0px 4=
px 16px; touch-action: pinch-zoom; }

.vk-box-blur { opacity: 0.5; transition: opacity 0.1s linear 0s; }

.vk-box.vk-min { padding: 2px; }

.vk-box.vk-sf-ie { border: 1px solid rgb(204, 204, 204); }

.vk-btn { border: 1px solid rgba(0, 0, 0, 0.1); width: 29px; height: 29px; =
margin: 2px; text-align: center; vertical-align: middle; position: relative=
; padding: 1px; min-width: 0px; max-width: 500px; min-height: 0px; max-heig=
ht: 50px; color: rgb(68, 68, 68); background-color: rgb(245, 245, 245); bac=
kground-image: linear-gradient(rgb(245, 245, 245), rgb(241, 241, 241)); bor=
der-radius: 2px; }

.vk-btn.vk-sf-h { border-color: rgb(198, 198, 198); color: rgb(34, 34, 34);=
 background-color: rgb(248, 248, 248); background-image: linear-gradient(rg=
b(248, 248, 248), rgb(241, 241, 241)); box-shadow: rgba(0, 0, 0, 0.1) 0px 1=
px 1px; }

.vk-btn.vk-sf-a { border-color: rgb(198, 198, 198); color: rgb(51, 51, 51);=
 background-color: rgb(246, 246, 246); background-image: linear-gradient(rg=
b(246, 246, 246), rgb(241, 241, 241)); box-shadow: rgba(0, 0, 0, 0.1) 0px 1=
px 2px inset; }

.vk-btn.vk-sf-s { border-color: rgb(204, 204, 204); color: rgb(51, 51, 51);=
 background-color: rgb(238, 238, 238); background-image: linear-gradient(rg=
b(238, 238, 238), rgb(224, 224, 224)); box-shadow: rgba(0, 0, 0, 0.1) 0px 1=
px 2px inset; }

.vk-cap, .vk-t { font-size: 14px; font-family: arial, sans-serif; font-weig=
ht: normal; line-height: 25px; }

.vk-cap { cursor: default; }

.vk-cap.vk-sf-b, .vk-t-btn { background-repeat: no-repeat; }

.vk-cap.vk-sf-b { width: 22px; height: 17px; opacity: 0.667; }

.vk-sf-ff2 .vk-cap.vk-sf-b { display: block; position: relative; left: 6px;=
 top: 0px; }

.vk-cap.vk-sf-b.vk-sf-h { opacity: 0.9; }

.vk-cap.vk-sf-b.vk-sf-c8 { background-position: -714px -16px; }

.vk-cap.vk-sf-b.vk-sf-c20 { background-position: -614px -66px; }

.vk-cap.vk-sf-b.vk-sf-c16 { background-position: -814px -16px; }

.vk-cap.vk-sf-c273 { font-size: 14px; }

.vk-cap-i { border: none; width: 20px; height: 20px; }

.vk-t { height: 24px; cursor: move; padding: 0px 3px; color: rgb(136, 136, =
136); display: inline-block; overflow: hidden; width: 100%; }

.vk-t.vk-min { width: auto; }

.vk-t-btns { margin: 0px; padding: 0px; position: absolute; display: inline=
-block; white-space: nowrap; top: 0px; }

.vk-t-btns.vk-min { position: relative; }

.vk-t-btn { margin: 0px; opacity: 0.4; height: 14px !important; width: 14px=
 !important; }

.vk-t-btn.vk-sf-hp { background-position: -670px -70px; }

.vk-t-btn.vk-sf-min { background-position: -720px -70px; }

.vk-t-btn.vk-sf-max { background-position: -770px -70px; }

.vk-t-btn.vk-sf-cl { background-position: -670px -20px; }

.vk-t-btn.vk-sf-th { opacity: 1; }

.vk-t-btn-o { padding: 13px 4px 8px; cursor: default; display: inline-block=
; position: relative; }

.vk-t-btn-o.vk-min { padding: 2px; }

.vk-t-btn-o.vk-sf-hp { cursor: pointer; }

.vk-ea-l { margin-right: 32px; }

.vk-ea-r { margin-left: 32px; }

.vk-ss { margin: 0px 5px; }

.vk-l-i { pointer-events: none; text-decoration: none; font-weight: bold; c=
olor: rgb(0, 0, 0) !important; }

.vk-l-a { color: rgb(0, 0, 255); }

@media screen and (-ms-high-contrast:white-on-black) {
  .vk-btn, .vk-btn.vk-sf-a, .vk-btn.vk-sf-h, .vk-btn.vk-sf-s { background-i=
mage: none; background-color: black; }
  .vk-cap.vk-sf-b { opacity: 1; }
  .vk-btn.vk-sf-a, .vk-btn.vk-sf-h, .vk-btn.vk-sf-s { border-width: 2px; }
  .vk-btn.vk-sf-a .vk-cap, .vk-btn.vk-sf-h .vk-cap, .vk-btn.vk-sf-s .vk-cap=
 { font-weight: bold; }
}

.ita-ff-black-enabled .vk-btn, .ita-ff-black-enabled .vk-btn.vk-sf-a, .ita-=
ff-black-enabled .vk-btn.vk-sf-h, .ita-ff-black-enabled .vk-btn.vk-sf-s { b=
ackground-image: none; background-color: black; }

.ita-ff-black-enabled .vk-cap.vk-sf-b { opacity: 1; }

.ita-ff-black-enabled .vk-btn.vk-sf-a, .ita-ff-black-enabled .vk-btn.vk-sf-=
h, .ita-ff-black-enabled .vk-btn.vk-sf-s { border-width: 2px; }

.ita-ff-black-enabled .vk-btn.vk-sf-a .vk-cap, .ita-ff-black-enabled .vk-bt=
n.vk-sf-h .vk-cap, .ita-ff-black-enabled .vk-btn.vk-sf-s .vk-cap { font-wei=
ght: bold; }

.ita-hwt-ime { overflow: hidden; width: 425px; height: 297px; background: r=
gb(255, 255, 255); touch-action: pinch-zoom; }

.ita-hwt-ime-st { position: fixed; opacity: 0.5; box-shadow: rgba(0, 0, 0, =
0.2) 0px 4px 16px; border: 1px solid rgb(204, 204, 204); transition: opacit=
y 0.1s linear 0s; z-index: 2147483640; }

.ita-hwt-ime-full { width: auto !important; left: 2px !important; right: 2p=
x !important; }

.ita-hwt-ime-opaque { opacity: 0.99 !important; }

.ita-hwt-ime-init-opaque { opacity: 0.99 !important; }

.ita-hwt-ime-hover { opacity: 0.99; transition: opacity 0.1s linear 0s; }

canvas.ita-hwt-canvas { cursor: url("https://ssl.gstatic.com/inputtools/ima=
ges/pencil.png") 0 10, auto; vertical-align: bottom; touch-action: none; }

.ita-hwt-grip { position: absolute; cursor: move; top: 0px; }

.ita-hwt-ltr .ita-hwt-grip { left: 0px; }

.ita-hwt-rtl .ita-hwt-grip { right: 0px; }

.ita-hwt-close { background-position: -660px -10px; background-color: white=
; width: 30px; height: 30px; position: absolute; top: 0px; cursor: pointer;=
 }

.ita-hwt-ltr .ita-hwt-close { right: 0px; }

.ita-hwt-rtl .ita-hwt-close { left: 0px; }

.ita-hwt-candidates { border-top: 1px solid rgb(204, 204, 204); background:=
 rgb(255, 255, 255); text-align: left; white-space: nowrap; }

.ita-hwt-candidate { display: inline-block; white-space: nowrap; height: 32=
px; line-height: 24px; padding: 6px 18px 3px; border-right: 1px solid rgb(2=
04, 204, 204); font-family: arial, verdana, sans-serif; font-size: small; c=
olor: rgb(34, 34, 34); cursor: pointer; }

.ita-hwt-selected { color: rgb(68, 68, 68); }

.ita-hwt-candidate-hover { background-color: rgb(240, 240, 240); color: rgb=
(68, 68, 68); }

.ita-hwt-candidate:active { background-color: rgb(224, 224, 224); color: rg=
b(68, 68, 68); }

.ita-hwt-disabled { opacity: 0.5; }

.ita-hwt-buttons { background-color: rgb(240, 240, 240); height: 60px; bord=
er-top: 1px solid rgb(204, 204, 204); }

.ita-hwt-button { display: inline-block; vertical-align: top; }

.ita-hwt-backspace { margin: 10px; width: 24px !important; height: 40px !im=
portant; }

.ita-hwt-backspace-img { background-position: -714px -118px; width: 18px; h=
eight: 14px; margin: 13px 4px; }

.ita-hwt-space { margin: 10px 0px; height: 24px; width: 296px; line-height:=
 24px; font-family: arial, verdana, sans-serif; font-size: small; text-alig=
n: center; padding: 8px 0px !important; }

.ita-hwt-enter { margin: 10px; width: 24px !important; height: 40px !import=
ant; }

.ita-hwt-enter-img { margin: 13px 4px; }

.ita-hwt-language { position: absolute; right: 0px; bottom: 0px; width: aut=
o; height: auto; font-size: small; color: rgb(117, 144, 212); }

.ita-hwt-clear-time { position: absolute; right: 30px; bottom: 0px; width: =
auto; height: auto; font-size: small; color: rgb(117, 144, 212); cursor: po=
inter; }

.ita-hwt-insert-time { position: absolute; right: 60px; bottom: 0px; width:=
 auto; height: auto; font-size: small; color: rgb(117, 144, 212); cursor: p=
ointer; }

.ita-hwt-enter-img-dark { background-position: -768px -120px; width: 14px; =
height: 10px; }

.ita-hwt-enter-img-white { background-position: -818px -120px; width: 14px;=
 height: 10px; }

.ita-hwt-grip { background-position: -700px -160px; width: 47px; height: 29=
px; }

.ita-hwt-grip-hover { background-position: -650px -160px; }

.ita-hwt-grip:active { background-position: -600px -160px; }

.ita-hwt-jfk { border-radius: 2px; cursor: default; font-size: 11px; font-w=
eight: bold; text-align: center; white-space: nowrap; padding: 0px 8px; }

.ita-hwt-jfk-hover { box-shadow: rgba(0, 0, 0, 0.1) 0px 1px 1px; }

.ita-hwt-jfk-standard { box-shadow: none; background-color: rgb(245, 245, 2=
45); background-image: linear-gradient(rgb(245, 245, 245), rgb(241, 241, 24=
1)); color: rgb(68, 68, 68); border: 1px solid rgba(0, 0, 0, 0.1); }

.ita-hwt-jfk-standard.ita-hwt-jfk-hover { box-shadow: none; background-colo=
r: rgb(248, 248, 248); background-image: linear-gradient(rgb(248, 248, 248)=
, rgb(241, 241, 241)); border: 1px solid rgb(198, 198, 198); color: rgb(51,=
 51, 51); }

.ita-hwt-jfk-action { box-shadow: none; background-color: rgb(77, 144, 254)=
; background-image: linear-gradient(rgb(77, 144, 254), rgb(71, 135, 237)); =
border: 1px solid rgb(48, 121, 237); color: rgb(255, 255, 255); }

.ita-hwt-jfk-action.ita-hwt-jfk-hover { box-shadow: none; background-color:=
 rgb(53, 122, 232); background-image: linear-gradient(rgb(77, 144, 254), rg=
b(53, 122, 232)); border: 1px solid rgb(47, 91, 183); }

.ita-hwt-butterbar { position: absolute; left: 0px; bottom: 100px; border-r=
adius: 2px; box-shadow: rgba(0, 0, 0, 0.2) 0px 2px 4px; border-style: solid=
; border-width: 0px; font-size: 11px; height: 0px; opacity: 0; visibility: =
hidden; overflow: hidden; padding: 0px; margin: 10px; text-align: center; b=
ackground-color: rgb(249, 237, 190); border-color: rgb(240, 195, 109); colo=
r: rgb(51, 51, 51); }

.ita-hwt-butterbar.shown { transition: opacity 0.218s ease 0s; border-width=
: 1px; height: 14px; opacity: 1; visibility: visible; padding: 2px 16px; }

@media screen and (-ms-high-contrast:white-on-black) {
  .ita-hwt-candidate-hover, .ita-hwt-candidate:active { font-weight: bold; =
border: 2px solid; }
  .ita-hwt-jfk-action { outline: solid 2px; }
  .ita-hwt-jfk { background-image: none; }
  .ita-hwt-jfk-standard.ita-hwt-jfk-hover, .ita-hwt-jfk-action.ita-hwt-jfk-=
hover { background-image: none; outline: solid 2px; }
}

.ita-ff-black-enabled .ita-hwt-candidate-hover, .ita-ff-black-enabled .ita-=
hwt-candidate:active { font-weight: bold; border: 2px solid; }

.ita-ff-black-enabled .ita-hwt-jfk-action { outline: solid 2px; }

.ita-ff-black-enabled .ita-hwt-jfk { background-image: none; }

.ita-ff-black-enabled .ita-hwt-jfk-standard.ita-hwt-jfk-hover, .ita-ff-blac=
k-enabled .ita-hwt-jfk-action.ita-hwt-jfk-hover { background-image: none; o=
utline: solid 2px; }

.ita-kd-btn-zh { background-position: -514px -18px; }

.ita-kd-btn-en { background-position: -564px -18px; }

.ita-kd-btn-dbc { background-position: -514px -68px; }

.ita-kd-btn-sbc { background-position: -564px -68px; }

.ita-kd-btn-zh_pun { background-position: -514px -118px; }

.ita-kd-btn-en_pun { background-position: -564px -118px; }

.ita-kd-arrow { background-position: -620px -218px; width: 12px; height: 15=
px; }

.ita-kd-floating-bar-icon { background-position: -670px -116px; width: 12px=
; height: 15px; }

.ita-kd-icon-button.ita-kd-left { border-radius: 2px 0px 0px 2px; }

.ita-kd-icon-button.ita-kd-right, .ita-kd-icon-button.ita-kd-mid { margin-l=
eft: -1px; }

.ita-kd-icon-button.ita-kd-single { border-radius: 2px; }

.ita-kd-icon-button { display: inline-block; min-width: 54px; text-align: c=
enter; color: rgb(68, 68, 68); font-size: 11px; font-weight: bold; height: =
27px; padding: 0px 8px; margin: 0px; transition: all 0.218s ease 0s; user-s=
elect: none; cursor: default; }

.ita-kd-inputtools-div { display: table; white-space: nowrap; }

.ita-kd-inputtools-div .ita-kd-icon-button { float: left; position: relativ=
e; z-index: 1; }

::-webkit-input-placeholder { color: rgb(153, 153, 153); }

.ita-kd-icon-button.ita-kd-small { min-width: 33px; width: 33px; padding: 0=
px; }

.ita-kd-icon-button.ita-kd-small.ita-kd-mobile { height: 30px; width: 44px;=
 }

.ita-kd-icon-button.ita-kd-dropdown { min-width: 18px; width: 18px; padding=
: 0px; }

.ita-kd-icon-button.ita-kd-dropdown.ita-kd-mobile { height: 30px; width: 36=
px; }

.ita-kd-icon-button.ita-kd-floating-bar { min-width: 14px; width: 14px; pad=
ding: 0px; cursor: move; }

.ita-kd-icon { width: 23px; height: 16px; }

.ita-kd-icon-span { display: inline-block; margin: 6px 0px 0px; opacity: 0.=
26; vertical-align: middle; }

.ita-kd-arrow.ita-kd-icon-span, .ita-kd-statusbar-icon, .ita-kd-icon-button=
.ita-kd-selected .ita-kd-icon-span { opacity: 0.54; }

.ita-kd-icon-button:focus { outline: none; }

.ita-kd-statusbar { box-shadow: rgba(0, 0, 0, 0.2) 0px 2px 4px; border-radi=
us: 3px; white-space: nowrap; direction: ltr; position: fixed; background-c=
olor: rgb(238, 238, 238); z-index: 2147483643; }

.ita-kd-statusbar-table { padding: 0px; margin: 0px; border: none; }

.ita-kd-separator { border-top: 1px solid rgb(235, 235, 235); margin-top: 5=
px; margin-bottom: 6px; }

.ita-kd-inputtool-icon:focus { margin-right: 1px; }

.ita-kd-dropdown-menu { background: rgb(255, 255, 255); border: 1px solid r=
gba(0, 0, 0, 0.2); padding: 6px 0px; margin: 0px; white-space: nowrap; z-in=
dex: 2147483645; transition: opacity 0.218s ease 0s; position: absolute; }

.ita-kd-dropdown-menu-mobile { position: absolute; top: 0px; left: 0px; bac=
kground-color: rgba(199, 200, 200, 0.5); width: 100%; height: 100%; z-index=
: 100; }

.ita-kd-dropdown-menu-mobile > .ita-kd-dropdown-menu { margin: auto; max-wi=
dth: 600px; position: relative; top: 50%; transform: translateY(-50%); }

.ita-kd-dropdown-menu:focus { outline: none; }

.ita-kd-dropdown-menu.ita-kd-ie { border: 1px solid rgb(204, 204, 204); wid=
th: 260px; }

.ita-kd-menuitem { display: block; padding: 6px 38px 6px 8px; position: rel=
ative; color: rgb(51, 51, 51); font-size: 13px; height: 16px; font-weight: =
normal; cursor: default; }

.ita-kd-dropdown-menu-mobile .ita-kd-menuitem { padding-top: 16px; }

.ita-kd-menuitem-inputtool-icon { width: 23px; height: 16px; display: inlin=
e-block; opacity: 0.54; position: relative; top: 3px; }

.ita-kd-menuitem-inputtool-name { line-height: 17px; padding: 0px 6px; }

.ita-kd-menuitem-setting { line-height: 17px; padding: 0px 22px; }

.ita-kd-menuitem-hover { background-color: rgb(241, 241, 241) !important; c=
olor: rgb(34, 34, 34) !important; }

.ita-kd-menuitem .ita-kd-checkbox { display: inline-block; width: 22px; hei=
ght: 16px; }

.ita-kd-menuitem.ita-kd-selected .ita-kd-checkbox { background-image: url("=
https://www.gstatic.com/inputtools/images/ita_sprite8.png"); background-pos=
ition: -614px -14px; background-size: 850px 250px; }

@media (min-resolution: 144dpi), (-webkit-min-device-pixel-ratio: 1.5) {
  .ita-kd-menuitem.ita-kd-selected .ita-kd-checkbox { background-image: url=
("https://www.gstatic.com/inputtools/images/ita_sprite8_2x.png"); }
}

@media screen and (-ms-high-contrast:white-on-black) {
  .ita-kd-menuitem.ita-kd-selected .ita-kd-checkbox { background-image: url=
("https://www.gstatic.com/inputtools/images/ita_sprite_grey8.png"); }
  @media (min-resolution: 144dpi), (-webkit-min-device-pixel-ratio: 1.5) {
  .ita-kd-menuitem.ita-kd-selected .ita-kd-checkbox { background-image: url=
("https://www.gstatic.com/inputtools/images/ita_sprite_grey8_2x.png"); }
}
  .ita-kd-icon-span, .ita-kd-menuitem-inputtool-icon { opacity: 1; }
  .ita-kd-menuitem-hover { border: 1px solid; font-weight: bold; }
  .ita-kd-statusbar { border: 1px solid; }
  .ita-kd-icon-button.ita-kd-icon-button-hover { border: 1px solid; }
}

.ita-ff-black-enabled .ita-kd-menuitem.ita-kd-selected .ita-kd-checkbox { b=
ackground-image: url("https://www.gstatic.com/inputtools/images/ita_sprite_=
grey8.png"); }

@media (min-resolution: 144dpi), (-webkit-min-device-pixel-ratio: 1.5) {
  .ita-ff-black-enabled .ita-kd-menuitem.ita-kd-selected .ita-kd-checkbox {=
 background-image: url("https://www.gstatic.com/inputtools/images/ita_sprit=
e_grey8_2x.png"); }
}

.ita-ff-black-enabled .ita-kd-icon-span, .ita-ff-black-enabled .ita-kd-menu=
item-inputtool-icon { opacity: 1; }

.ita-ff-black-enabled .ita-kd-menuitem-hover { border: 1px solid; font-weig=
ht: bold; }

.ita-ff-black-enabled.ita-kd-statusbar { border: 1px solid; }

.ita-ff-black-enabled .ita-kd-icon-button.ita-kd-icon-button-hover { border=
: 1px solid; }

.kd-bubble { background: rgb(249, 237, 190); outline: rgb(240, 195, 109) so=
lid 1px; box-shadow: rgba(0, 0, 0, 0.2) 0px 2px 4px; padding: 16px; border-=
radius: 2px; width: 300px; }

.kd-bubble a { text-decoration: none; color: rgb(17, 85, 204); cursor: poin=
ter; }

.kd-bubble p { color: rgb(102, 102, 102); margin: 0px; font-size: 13px; lin=
e-height: 18px; }

p.kd-bubble-links { margin-top: 10px; }

.kd-bubble-pointer { outline: none; display: block; position: absolute; top=
: -11px; left: 24px; margin: 0px 0px 0px -5px; width: 17px; height: 11px; b=
ackground: url("image/bubble_point_yellow.png"); }
------MultipartBoundary--ZeJbom7ua2thyClsILZ3bxA8NwD3gXWgKq2ZLWICWB------
