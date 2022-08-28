From: <Saved by Blink>
Snapshot-Content-Location: https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-DB0201EN-SkillsNetwork/labs/BonusModule_Coursera_v5/Hands-on-lab-Joins.md.html?origin=www.coursera.org
Subject: 
Date: Sun, 28 Aug 2022 17:36:33 -0000
MIME-Version: 1.0
Content-Type: multipart/related;
	type="text/html";
	boundary="----MultipartBoundary--jI1qYAMiE8p0qZCDyE3LEZb4aub2Deq1TfPgMJPE3x----"


------MultipartBoundary--jI1qYAMiE8p0qZCDyE3LEZb4aub2Deq1TfPgMJPE3x----
Content-Type: text/html
Content-ID: <frame-FAB2A281B23DD06AA1EDAE5764F9EEFC@mhtml.blink>
Content-Transfer-Encoding: quoted-printable
Content-Location: https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-DB0201EN-SkillsNetwork/labs/BonusModule_Coursera_v5/Hands-on-lab-Joins.md.html?origin=www.coursera.org

<!DOCTYPE html><html lang=3D"en"><head><meta http-equiv=3D"Content-Type" co=
ntent=3D"text/html; charset=3DUTF-8"><link rel=3D"stylesheet" type=3D"text/=
css" href=3D"cid:css-f07009bc-28dc-453b-9c56-5d0d9f1055c7@mhtml.blink" /><l=
ink rel=3D"stylesheet" type=3D"text/css" href=3D"cid:css-3e257d17-a1b3-4e75=
-920d-34ade98c404a@mhtml.blink" />
   =20
    <meta name=3D"viewport" content=3D"width=3Ddevice-width, initial-scale=
=3D1">
    <link rel=3D"stylesheet" href=3D"https://stackpath.bootstrapcdn.com/boo=
tstrap/4.3.1/css/bootstrap.min.css" crossorigin=3D"anonymous">
    <link rel=3D"stylesheet" href=3D"https://unpkg.com/@highlightjs/cdn-ass=
ets@10.7.1/styles/default.min.css">
  </head>
  <body>
    <img style=3D"float:left;" src=3D"https://cf-courses-data.s3.us.cloud-o=
bject-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-DB0201EN-SkillsNetw=
ork/labs/BonusModule_Coursera_v5/images/IDSNlogo.png" width=3D"200" height=
=3D"200">
    <h1>Hands on Lab: Joins</h1>
    <p>Estimated time needed: <strong>30</strong> minutes</p>
    <h1>Objectives</h1>
    <p>After completing this lab, you will be able to:</p>
    <ol>
      <li>
        <p>Determine the correct type of join to use for a given problem.</=
p>
      </li>
      <li>
        <p>Write and execute joins to query data from multiple tables.</p>
      </li>
    </ol>
    <h1>Scenario</h1>
    <p>In this hands-on lab, you will work with three datasets that are ava=
ilable on the City of Chicago's Data Portal:</p>
    <ul>
      <li>Socioeconomic indicators in Chicago</li>
      <li>Chicago public schools</li>
      <li>Chicago crime data</li>
    </ul>
    <p>You must download each dataset, create a table for each one, and loa=
d the appropiate dataset through the Db2 console. You should not reuse simi=
lar tables with other names from other exercises or labs, as they may not c=
reate the correct results.</p>
    <p><strong>Important note:</strong></p>
    <p>
      If you have <b>not</b> yet downloaded the three datasets from the Cit=
y of Chicago's Data Portal,
      created the required tables, and loaded the data, please follow the i=
nstructions in this section.
    </p>
    <h2>City of Chicago Datasets</h2>
    <ol>
      <li><strong>Socioeconomic indicators in Chicago</strong></li>
    </ol>
    <p>
      This dataset contains a selection of six socioeconomic indicators of =
public health significance and a =E2=80=9Chardship index,=E2=80=9D for each=
 Chicago community area, for the years 2008 =E2=80=93 2012. A detailed desc=
ription of this dataset and the original dataset can be obtained from the C=
hicago Data Portal at:
      <a href=3D"https://data.cityofchicago.org/Health-Human-Services/Censu=
s-Data-Selected-socioeconomic-indicators-in-C/kn9c-c2s2?utm_medium=3DExinfl=
uencer&amp;utm_source=3DExinfluencer&amp;utm_content=3D000026UJ&amp;utm_ter=
m=3D10006555&amp;utm_id=3DNA-SkillsNetwork-Channel-SkillsNetworkCoursesIBMD=
eveloperSkillsNetworkDB0201ENSkillsNetwork20127838-2022-01-01" target=3D"_b=
lank" rel=3D"external">https://data.cityofchicago.org/Health-Human-Services=
/Census-Data-Selected-socioeconomic-indicators-in-C/kn9c-c2s2</a>
    </p>
    <ol start=3D"2">
      <li><strong>Chicago public schools</strong></li>
    </ol>
    <p>
      This dataset shows all school level performance data used to create C=
PS School Report Cards for the 2011-2012 school year. A detailed descriptio=
n of this dataset and the original dataset can be obtained from the Chicago=
 Data Portal at:
      <a href=3D"https://data.cityofchicago.org/Education/Chicago-Public-Sc=
hools-Progress-Report-Cards-2011-/9xs2-f89t?utm_medium=3DExinfluencer&amp;u=
tm_source=3DExinfluencer&amp;utm_content=3D000026UJ&amp;utm_term=3D10006555=
&amp;utm_id=3DNA-SkillsNetwork-Channel-SkillsNetworkCoursesIBMDeveloperSkil=
lsNetworkDB0201ENSkillsNetwork20127838-2022-01-01" target=3D"_blank" rel=3D=
"external">https://data.cityofchicago.org/Education/Chicago-Public-Schools-=
Progress-Report-Cards-2011-/9xs2-f89t</a>
    </p>
    <ol start=3D"3">
      <li><strong>Chicago crime data</strong></li>
    </ol>
    <p>This dataset reflects reported incidents of crime (with the exceptio=
n of murders where data exists for each victim) that occurred in the City o=
f Chicago from 2001 to present, minus the most recent seven days. A detaile=
d description of this dataset and the original dataset can be obtained from=
 the Chicago Data Portal at: <a href=3D"https://data.cityofchicago.org/Publ=
ic-Safety/Crimes-2001-to-present/ijzp-q8t2?utm_medium=3DExinfluencer&amp;ut=
m_source=3DExinfluencer&amp;utm_content=3D000026UJ&amp;utm_term=3D10006555&=
amp;utm_id=3DNA-SkillsNetwork-Channel-SkillsNetworkCoursesIBMDeveloperSkill=
sNetworkDB0201ENSkillsNetwork20127838-2022-01-01" target=3D"_blank" rel=3D"=
external">https://data.cityofchicago.org/Public-Safety/Crimes-2001-to-prese=
nt/ijzp-q8t2</a></p>
    <h3>Store the datasets in database tables</h3>
    <p>The lab requires you to have these three tables populated with a sub=
set of the whole datasets. Download the 'ChicagoCensusData.csv', 'ChicagoPu=
blicSchools.csv', and 'ChicagoCrimeData.csv' datasets below and load the da=
ta into your Db2 On Cloud database.</p>
    <p><a href=3D"https://cf-courses-data.s3.us.cloud-object-storage.appdom=
ain.cloud/IBMDeveloperSkillsNetwork-DB0201EN-SkillsNetwork/labs/BonusModule=
_Coursera_v5/datasets/ChicagoCensusData.csv">Chicago Census Data</a></p>
    <p><a href=3D"https://cf-courses-data.s3.us.cloud-object-storage.appdom=
ain.cloud/IBMDeveloperSkillsNetwork-DB0201EN-SkillsNetwork/labs/BonusModule=
_Coursera_v5/datasets/ChicagoPublicSchools.csv">Chicago Public Schools</a><=
/p>
    <p><a href=3D"https://cf-courses-data.s3.us.cloud-object-storage.appdom=
ain.cloud/IBMDeveloperSkillsNetwork-DB0201EN-SkillsNetwork/labs/BonusModule=
_Coursera_v5/datasets/ChicagoCrimeData.csv">Chicago Crime Data</a></p>
    <p>You need to create a new table for each dataset. As you load each da=
taset, click on "(+) New Table", specify the name of the table you want to =
create, and then click "Next".</p>
    <img src=3D"https://cf-courses-data.s3.us.cloud-object-storage.appdomai=
n.cloud/IBMDeveloperSkillsNetwork-DB0201EN-SkillsNetwork/labs/BonusModule_C=
oursera_v5/images/LoadingData.png" width=3D"800">
    <p>Name the new tables as follows:</p>
    <ol>
      <li>CENSUS_DATA</li>
      <li>CHICAGO_PUBLIC_SCHOOLS</li>
      <li>CHICAGO_CRIME_DATA</li>
    </ol>
    <p>After you have created the tables, review the data in each table by =
using the View Data feature in the Db2 On Cloud console.</p>
    <h2>Problems</h2>
    <p>When you have confirmed that the three datasets are loaded into the =
CENSUS_DATA, CHICAGO_PUBLIC_SCHOOLS, and CHICAGO_CRIME_DATA tables, you can=
 proceed. Write and execute SQL queries to solve the problems below.</p>
    <h3>Problem 1</h3>
    <h5>List the case number, type of crime and community area for all crim=
es in community area number 18.</h5>
    <details>
      <summary>Hint 1</summary>Use tables CHICAGO_CRIME_DATA and CENSUS_DAT=
A.
    </details>
    <details>
      <summary>Hint 2</summary>Use an inner join.
    </details>
    <details>
      <summary>Hint 3</summary>The column PRIMARY_TYPE contains the crime t=
ype.
    </details>
    <h3>Problem 2</h3>
    <h5>List all crimes that took place at a school. Include case number, c=
rime type and community name.</h5>
    <details>
      <summary>Hint 1</summary>Use tables CHICAGO_CRIME_DATA and CENSUS_DAT=
A.
    </details>
    <details>
      <summary>Hint 2</summary>Use a left join or a right join.
    </details>
    <details>
      <summary>Hint 3</summary>The column LOCATION_DESCRIPTION will help yo=
u find the crime location.
    </details>
    <h3>Problem 3</h3>
    <h5>For the communities of Oakland, Armour Square, Edgewater and CHICAG=
O list the associated community_area_numbers and the case_numbers.</h5>
    <details>
      <summary>Hint 1</summary>Use tables CHICAGO_CRIME_DATA and CENSUS_DAT=
A.
    </details>
    <details>
      <summary>Hint 2</summary>Use a full outer join.
    </details>
    <details>
      <summary>Hint 3</summary>Use COMMUNITY_AREA_NUMBER from CENSUS_DATA.
    </details>
    <p>Copyright =C2=A9 2020 IBM Corporation. All rights reserved.</p>
    <h2>Author(s)</h2>
    <h4>Ramesh Sannareddy</h4>
    <h2>Contribtuor(s)</h2>
    <h4>Rav Ahuja</h4>
    <h2>Change log</h2>
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
          <td>2021-01-29</td>
          <td>1.2</td>
          <td>Rav Ahuja</td>
          <td>Fixed license statement</td>
        </tr>
        <tr>
          <td>2021-01-28</td>
          <td>1.1</td>
          <td>Rose Malcolm</td>
          <td>Converted to markdown. Added instructions to skip table setup=
 if done in previous lab.</td>
        </tr>
        <tr>
          <td>2020-11-25</td>
          <td>1.0</td>
          <td>Ramesh Sannareddy</td>
          <td>New lab created</td>
        </tr>
      </tbody>
    </table>
    <h2></h2>
    <h3 align=3D"center">=C2=A9 IBM Corporation 2020. All rights reserved.<=
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
------MultipartBoundary--jI1qYAMiE8p0qZCDyE3LEZb4aub2Deq1TfPgMJPE3x----
Content-Type: text/css
Content-Transfer-Encoding: quoted-printable
Content-Location: cid:css-f07009bc-28dc-453b-9c56-5d0d9f1055c7@mhtml.blink

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
------MultipartBoundary--jI1qYAMiE8p0qZCDyE3LEZb4aub2Deq1TfPgMJPE3x----
Content-Type: text/css
Content-Transfer-Encoding: quoted-printable
Content-Location: cid:css-3e257d17-a1b3-4e75-920d-34ade98c404a@mhtml.blink

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
------MultipartBoundary--jI1qYAMiE8p0qZCDyE3LEZb4aub2Deq1TfPgMJPE3x----
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
------MultipartBoundary--jI1qYAMiE8p0qZCDyE3LEZb4aub2Deq1TfPgMJPE3x----
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
------MultipartBoundary--jI1qYAMiE8p0qZCDyE3LEZb4aub2Deq1TfPgMJPE3x----
Content-Type: image/png
Content-Transfer-Encoding: base64
Content-Location: https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-DB0201EN-SkillsNetwork/labs/BonusModule_Coursera_v5/images/IDSNlogo.png

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

------MultipartBoundary--jI1qYAMiE8p0qZCDyE3LEZb4aub2Deq1TfPgMJPE3x----
Content-Type: image/png
Content-Transfer-Encoding: base64
Content-Location: https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-DB0201EN-SkillsNetwork/labs/BonusModule_Coursera_v5/images/LoadingData.png

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
uyHFJ9oapZBoTDNkt/atGKV6dX5RhboNVbJ2fRWpXEf5jfmby5C3Ui3lKPuzyrWcoIkecbpqG9X0
zJ5O/icUvHmEmrdprUI1Gqpc3QYqUrWu8pnTNeaRt1J15a7QSHm/G6thO6/qsm20lGvmIZE3pZOz
NXVIZxWs3lBl6/ysQu2m6ce5F+QXFGNrZD7PS7pwdK66fFdXZUpVV85K5rx+sJahxI/NjPXSRGWM
51nUWNf5Kxvru2xV5avyg2pNP6nZF6S4+6vqXrDktlgO47urSK3GKl3LWDetxui7qWd13jfK1ggA
AAAAAAAAAOD389KLXoGuu+XQKKvypH9XaTJX1Yc9jmv+qZSFqlQkBSki8LT27FiqHvXqqWSWQsrV
sJVKtu6mOs3b6sfWdZS7XC29l6WNmo1ZoVXu1+VhTDLaNvpjPLbqwqiKypU7q9K89YXSfJxFabJ2
VuG+u3UtIZV+VAlRUsByrRxZT599kEFp/pVL/8hVVXmbdVCVVp1Vp0Un1W7ZSZXKfaeSJauozIjl
6r3dUwe84nUvzjaNp7m+Vf6zf1S2XN8qzTs59D8ZKytXneaq2qazajXvoLqtO6tynWbKZTxeqeNg
9Tl0Qi6+iXqovpeSv4eC5v6k+uXN6aVTmve/Upr0DfRBAyft9L1ra2RWrK7rmusqjWzZUY0atlX1
lu1Vu1UzFStdSl988Y3+56Ns+kfeqsr6kzH/psZzbNJKtYzn2n65u1ZeS1EfDL2piOXN1blGLqV5
L72RL5UmXQ39+fslWnk+8EmlOQAAAAAAAAAAgNfmpRe97rgf0Oo2hVQq91f6S4F6yjDotJa5Pq3o
lSSFuuiEY0cV+LaA/vxuFWWqPlGzgiLkZQ2PN3JK+1cPUM1v8uqDDwoqY4OR6ueeII/7nZoe4b1n
ueb+/K1y5MmtP2XIp3eyFNSfPq2tfL/M1uJ7cfKztXsgMUq67aR1k5oqyzf59ecP6qhwuyVaaSxa
oK2JKfroUrn0LKXMObLr/1Xoo+LTveUWYC7fM3jtVMCipipcvKDSfFVTH1edrUXn/BVmG2wK97mg
bT3KqWref+utfNVVcpavHK7ZBj4i+PJJOXcopkpFsuvPGfLr7Sx59Zd/V9aXxQdr9BV/XbC1e5xZ
8PPVgfn91Trft/ooXSnl7bZEE3ykgKdcUzHi1jW59K6sH0pk0V8zFtC/MufR374srw9z9VDfo9d0
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
0nNPaNmL+3OzDi1spiyxE+mdMMUUt8JkLX8gHd0+WdMrxfPup0j6KH9HZR99TUv6Ntaw0rH0vs2z
VmKUqs666zuG7/H8lnePrNLSGaPVpXNXNW7aQjUbN1HFRo1VrE4D5c2bR6njJNSHX+RRllb9NeTq
erWsUliZvoitD2OUUdEx27Xwpcfe//4FrW6eWyUShNeHcXMpx7izGrhgs9Y0TKFMCb/WX5OUUoKO
B7Xg5fvKf7+ebPH6PWMK/T1CIX2aY6AWjmqlGT0K6UMLvcKVU4qq07Xu6dOA+d9e6f7nurxusuYP
bKXGHbqq0eTt6j1uoWZVSaPcSaLrH7GyKmLpXqrWc4omz5yt8TPmacLwfhrSorxy5syiOMVbKdfQ
U1o/eYA2tsus8LHi6o/JGih1m23aH5hYPn+oo8Oqq1m2yN7xJFOMZivVef19+Z9eqeUD66lY5uQK
EzWBPo6bXbFy1VDe+h1Vs9sE9Zy4VXu9r7hnj0/r4cL6qpY3mf4RJZs+KD5FfVZ++5Q+2DVPa5uk
UpJ4kfX3dHWUtM8Z7TmwX7fWD1Hz0tmUIJ7NH5hSX6cto7Tlm6l8+4FqPnCJ5u644gvJN2j7jEbK
GC2RPnw3haLmaaN2Rx9qv1v2sge6PquVepdK6uZSC5WwlbI1X6DDp1ZrzYrJ6tmth5o2874rvetf
qXFjlajbSPkKFVL6+An18eeZlbDCUPW/5v1LcXON929INSWNm1D/F62iYtVcpB03Am/W6zqxbr5m
D+mjjh3bq1bT1qpUp7kqV6+nKpVKKX/+jPoqWiy9k7Gpknc7qMNXX/tfHlzdp2tTK6tMtoT6a+Ts
+rzkDPVf/yPx08NDOrHM65Mf6qtdVwP66sQkrehcUOGiJdBfcg1Sgb6bdHtbbw2tl1XhwyfW+1n6
qM6UIy6QDOJfQAAAAAAAAOA3KwSHXv46Mq6xOpfKrM9KTVW3ZTZgmL1FPqiVIxqrfII0KjrkkEae
diu/6soi7ZvYSEni1lHFIcu12O+ERtXKrmrl6inv1Pva7coFAp3Sqa1DVCt5CuWvO1Yt9kjXXs7E
zM1Duryik+qXzq+Y8dMrdqZCSlq4hvLU7KDaXQarVoUSKpY1rRK3Wateu7z1/e9rf7+yalSmsCK2
2KE5+78d6u7J1nFa2yqLoqfMrA/iZVL81JkV0/vvqCkyK1qKLIqWMrtipMqhBJmLqFj/1Rp2VAFz
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
qbX4GXO7frT7PLt3j1y9ccP10b37D1xgF1SQZ/uev3Sl8pWp5vrchl+1c7JrENu7R/KXraYJM+bq
wcNHvk986+btO1qwbLUKVaylT73+tH60/rR+tOFEv/S+52xb1tfZipbXjHmLdeXqzx/0AwAAAAAA
AMDPgdDrDdhcXJNmzVOERGncy+54GXKpVbc+WrNpq6u0+G89fPRIsxcuU+maDV2g8U742Ar1/lcK
9Z8vFOqdzxXqvTBuvzbsWbnajTVz/hJduhJ02PGmodfVazc0d8kK9yLeXv7/86sYAUOrvWP79tq7
X+ofX0V3L/pLVK2nKXMWBFnBEsiqo+YtXeGCq2TZC+r9SPEVKnQE37kEtD99Gklh46d2QdDgsZNc
dY6xIGjZmg0qUL6GQv3zE/eZv4WJ5l7EW2Dyty+juuMJ9cf39O/wsdSu5wBXbfMmrK8thLKqsaTZ
Cug/Eby+tm3a8f3b6+v/eP/9UXj34j9lriLuPFZt2OL79Jt709Dr2TN/bdq2y+3Xwk8LeUJ95PVf
4PXwjvMPXn/a8VmA1aJzLzevlQUgQbH704LEZh17KEXOwvrP13EU6sNw3ra8cw3cpne+70WM64LV
Oi3aa8mqtT8aptk+rQ8TZ8kfcI3tnrG+s+1+GF4fePdeoQo1XQVR8049XXWWVRG9aehlwVrLLn0U
MXF6hfrHx/q/TyJ61yyO68t/hYupP3z8dcA5hHpHMb37187VrnEgq5Cas3iFajVrp4SZ87rPuGfL
rnVgf3rbsO2lyVPM21cvV631ehViIKs2e9frq1B/+dA9EwuWr1LvoaOVIGNu7/6M5n4e6oNwquE9
d1atGBh6WUWcBWHZi1XwvkfSuWfgRf97zY7hXe/a2HNu9+XUOQu/95o+euynA4eOuufcQmULraxf
Avrftuedm3ePfOLdI2nyFlML75y+OfLqc2KVW5NmzndhZKg/f+DuiX+Fi+X6wY4j4Pi87XjPWuSk
GTV8wlSdvxh0tRkAAAAAAAAA/K8Rer0hq9rIXLi0eyFszSpEytRqpLmLl7sX0GcvXHRDmllYYEFD
cIcCu3v/vpuXyEKRP3wcwYUFVjVjL9ETZc6nRFnyKUGmPK76yF5i//mzyMpTuoqmz1vkhgJ83ZuE
XvcfPNCcRcvdkGr2sv29SPEUKWkGV4nl9u21hN6+7eW+VVfZ8WUpUlbL127U7SD2bS/45y1d6bb3
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
9uk17di1l3tcx649Xf9Ux45vgdef1HO0+r6LzZqfcHV0Uq+d+q3qr2p5XfsMtH0HDgZ/E7Brz153
TLX0lqfmr7Pf/O3Q842fOiPJ54nWpfaVjpFvvdumzZ5vR44dDz4qaVqfLd77cezk6e49McQ71tZ4
x+e5YD9ev9dzTp8z3y1bx53/XK2890T7zj3sO29/t/6xa/x66LXQ7/SY8P0l0+cscK9Vm5+6RXw9
AaQPQi9kVlkm9FLlVqR1jabddx/BF4CYIvRCTKR36HXk2DErULaq/ecN99ifb3/YnUDSCYZIB72+
OOtkxGv5itsjr7xjsxcsDv7mYtt37rZXPixiz7yV25q0/s527tnrbr/gLVdBWO6SFe0vdzxqf/Ke
89oHn7VrH3jGtX898LT9/e7H7ak3PrC6Tb611es3usf59EVeJ9wq1vnC/nDrg/an2x527c+3P+L+
nav4x275DZq1sRx5itn1D2Wz/7v3ycDyvef5612P2f/e8oD9zfv5z/uecrdf4/287qFn7YnXc7mT
GgAApFSk0EsBloY3rFixoq1cudJ9toaGWWq6mGPDhg1WpUoVN7zh6dOnM2yl16EjR10Y8VbBkvav
+59O+Hz12r9fe5c9/eaH7sIW8fsRCp7mLV5qD72U0/1+yYpV3n6J3OeJ87ZdJ9vvejaHvfRBIVu5
NrCNCsIUnrzwbn778x2PuM9x9R/UX/jvm+6zmg2bufuFm7NwsT2bM4/7vL/GW99/eev5T2+dr384
mz3zZm538v5UXPIn6nTi//1i5ez3191tf/OeT+GCgrtLfTU4cOiw6zPlLFTqon31nzfc6/bH8HGT
3P2S+qKhddM6al21zlp3t4wHn7H/uvE+u/mxF2zq7HnuvjqOrpRCR+3Lf7/ursD6es+jfaY+02M5
3rOaXzazZavWBO8dsGPXHitbvZ7d+fSr9sdbH/L2tR6X0K9TH0vLeNjb3lre4/0g0/dD9z6uD/fH
2x5y/VD9VHvklXftM68fuHz12uA9zetPdrTf/P0W+80fr7ePa9b3vqwlv82r1220+55/w37z+7+7
/qACtlDadzqGdOxqe7We/nq7dfdeN23LLY+/6Lb9SvfxpfaV1kXrUbZGPRs/ZYYdv0SgqeNGQfO7
Rcq4ffa89/5QOKv+uvzira/69Aot/3HPE275/nPp33/x3ktaD3d7cD3+cuejdtsTL7l9rQvhwqn/
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
mzFvoS1attJ27t5rZ8+dCz4qMS1j3cbN3jJW2ly3DD02YTkzvWXMXbTU1mzYZEeOHgs+6mJ6k23a
us1mzQ88NvBzkfu5fefu4L0SnPfuv+/AQZvnLXu2d5/5S5a7psfOXbTEtu3YZSdPxbn7/vLLBXdf
bcuyVWvc9iT1Rj5//rzt3rffFi5dYTv37LVz3r9D6XE7d+8JWceE7dTzb9i81U6fPuPuq9dx45Zt
bj/62xNYv6XefZfZgqXL3T7zlzNjbmAZWr+4uNNuGaH2HzhkK9esd4/VdmzftdvtNwBAxnK1VHod
9j7X13p9AH0Oh38m6vMq3IULF7zP5lO2Ys06W7Vug52Ki7MLSXwe677HT5y05avW2pr1Gy3udOBz
8Yz32ap+gfouek59luqzU/2Y6XMW2CbvczcSfb7rOfUZ7K+rfupxK9eut4OHDgfvmTR95m7YstU9
38JlK+yA9xitZzQOHzlqa72+UKR9tXz1Wm9fXPy5H07rqHXVOicsY5Fbhvo4qdV/VF/nzJmzro+o
flagjxhY39Cm59U+1WsS6tDhI65vqO1V/ys56q9p3Xfv3R/ff5ITJ0/Z+k1b3Ousfl3gORPvN/Wh
Vq/baIe8fRtOr5VeHy176/adrh+b3Jc4HYs6lhcEjyX1A+ctXub+W/sgUl/0nLfM3Xv32Xzvflqf
0HXTcZlcvzeldJxt8V4Pve7hx4/WddPW7Un21X16T4aup1uO17Tdei+H0/rrdVQffu++A8FbI4vm
Nf9F2+C9Fou87wyz5nvr4bYjsC1aL21ftLTf5/jbEFyG+tvaF9t37bnomPTpb4qOK/1NSe77QDj1
y/U+De23h67/rj37gvcE0l9MQi8aLaM0AMAVIfRCTMQ69NIXzGqfN7EHs79t19z/lF37wDN27YMJ
7a93PmqP5XjPGrXs4MKcSLSMIuWr2wMvvpXw+JDl/OOeJ+zWJ7LbBx+Vt+FjJwUflZjeVDt277Hy
tT53z/mvB5722jP2r/uftj/d9rDVb9oqeM8ECtv6DR1ldz79iv3trsfslsdfdE3Pd9uTL1mT1h1t
1doN7r4nTp60nwcMsbufzWFPvfGhNW7VMT4QC6X10ImTDl172u1PvmwtOna66ISWft/YW/b/ec/z
f/c+Gb+tet57sr1mxSp+6k7QiMKxGl98bX+54xH7Z/x9n7UbH3nOrav2yw0PPxe/jD9797v/hTet
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
HYVb8z/vZ33uqmI9b61gy1qOtDMHCb2ipdBL1VsLFiywAQMGuCBLPxVy7Ny5M3ivAIVefkCm+wwf
PtzWrl0b/G3qU5iz7aDZT9PN3mhl9r+aU0vD+ykAKmx2c9Wj1rjTNBszvL/16DfCnq67y/6rzPlA
qJTawZf3fP+savbFsMA8XtsPmT3bxLs9POzyW1qEXkUD4Z/mIes112z3Ee/4D+yqNEfoBQAAAAAA
AADIlOJDr5e+cKHXqLe/dvN6yS+nz7r5u07vP2Y7Jq2wycU7uPv0vruKLW87xt0nliKFXqcJvaIW
KfQaOHCgq/aaM2dOouAr1qHXmXNmC7eajVhm9s14s2uqe7s4v9cUGhU0u67ycWvSeZqNGDrQfuw1
xh6utS8wt1dwqEE3f1dqNe/5bv40EDbNWG/WfrLZjTW82zXcYKT7p0XoVcjs3npmbSaYDV9qtmx7
oCIuFgi9AAAAAAAAAACZUnjoNfqdpnZ45Y7gbxMc37rfZlXrbt3/Vdq6/auMLW6WcC78118uWNyB
Y7Zz8kpb03myLW8zypa1Gunm3NK/985db+dORJ6M6MK58y5kW/fzNFvRYax73PK2o21Nl8m2Z/Za
O3c8LnjPJCq9Dp90v/vlzDk7smaXW87SFsNt1fcT7Mi63d66XWEgFiGYiG/JyAyhlz+vl8KvESNG
2NKlS+38+fPuvtGGXpoLbP/+/W5esDVr1rghEPVz48aNtmfPHvec8uuvv7rhErdu3eqWo/uEhmxn
zv9qq3acsWlL91qfcWusTJtV9kSt7XZz1WP20uf/v707j47qvM84np4mbZO0PW2apmmTLk7j2DU2
TtLUaZ32JE3SJWn25MRtMKQOm+KCjWzHNraJjZ3YAYwXMF6IF1ataEECtCCBQEhIoBUkxCok9kUS
iyTQBk/v7525Y4Gvx47ZRuPv55znjDRz586ge/nrOb/3bdWdszbq5aQVys7K0KK0XN0zp1KjZmzW
Vx/ZrT9I6A0sl95xRkl/PEG65QVpxFzpn5+Q3p8Qej7w+EtRev1I+uqT0ibvv6JNm9meYpdjaUND
6QUAAAAAAAAAGJLeUHp941dqq28Jvxpi014ndx9R+d2h0mv+x8ardvrS8KtS96Hjas7e6PYAS73h
bi2+eqIWXXW7K6aSr52kssR5OljW9Ibiyz77aO1uld+zQOl/f5+SPnWHe9/iT05Q8nWTtHbCy9pf
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
1xM6UrXLvWYTXFZo9XWeVtumFjdJZftmLfirBFU/nhUZzDp1+Lh2pVe4qSvbh8smr6yUsr23krws
/JvbXZlW7k96nTmrzbPzlP2lh13pVXH/Yh2tbv7NSq9r7gjtB3b1RPdok2i29OLBcitxzp04uyAB
xUQkUQyV0svKK58tSeiXULa3l/0brPyy4spKLyu2jE112SSYFVX2mhVlQbHXbQlDO5ctmWj7eQ12
+PBhN+FlfyP7XFti0fYT83X3So37pSlLpTEvtuuFRYXKzYrv0mt2sbTzsHT6Mi9pOBilFwAAAAAA
AABgSDqn9PrLBDflZRNb57PCqW5mriuzXvvIaK29/WW1N+5V94Fjas6sVP73ZmjJTZO17Gu/dMXU
plkrVPOrLBWPmu2msFKvv0tlifN1uCJUetneW0u//A4nvbxz2few5Rft81Z881dK+8zP3DTZ+nsX
6tD615fhu2ABxUQkUQyV0quxsTH8amj6ypYktNIjKytLRUVFWr58uSuvBk969fT0nDPpVVJS4qa8
rDSzR8vu3bvV2trqSiybIrM9v/r6Xm9ybB8x+7v4JZudxya9bPLMilbT1Ss1HZRq9kora9r1Skqh
MpfEd+m17ZC03UvPFVjW0EfpBQAAAAAAAAAYks4vvaxAatvUGn71XE2vrFL6Z36mhX/1U60e/bz2
FNRp36oGVUxOcpNWVkJVTU3XyZbQumynDh3X5jn5bk+vlOsSVZZoyxvukM6e1fbFpcr77nRXetnz
h8q3uVLLN9DTp1NHTsj29bLvaPzSy85l011FI2ap7skcbZq9QoX//bQWfSK0zGH908veskB72wKK
iUiiGIqll+251dzcrFWrvOvsve5Pa9nj4NLL7cm2Y4d73ia97Hxvxt/ja7DBe3pZuWYli53fpsLK
ysrU1tbmfcaATvWF9rXq7pf2HmhXcmahsjNS9eKiQXt6xVnpZRNere3e/x0mvQAAAAAAAAAA+M0E
lV7tm/eEXz1X44uFbulCK7hs0mv/6kZtfW21m+ay8mrVj5/T7uyNkfKq93i3Gl9a6aaxrKhyyxtW
hJbIs88snfiKm9gq+P6T2rG4NPI+e+zYstdNi5VOfDWyf5g9v/HnqW7ZRCu4aqcvVde+dvUc71Lt
tGxXxi342HitGT9XbfWtGrgYa8QFFBORRDEUSy9j01jV1dXnLFF4full9u3b556zf58tgTh4vy5j
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
AAAASUVORK5CYII=

------MultipartBoundary--jI1qYAMiE8p0qZCDyE3LEZb4aub2Deq1TfPgMJPE3x----
Content-Type: text/html
Content-ID: <frame-1271F58207F3AE372E28935460F4D587@mhtml.blink>
Content-Transfer-Encoding: quoted-printable

<html><head><meta http-equiv=3D"Content-Type" content=3D"text/html; charset=
=3DUTF-8"><link rel=3D"stylesheet" type=3D"text/css" href=3D"cid:css-5afcf6=
30-2125-4dc7-96b8-26f5b199550c@mhtml.blink" /></head><body></body></html>
------MultipartBoundary--jI1qYAMiE8p0qZCDyE3LEZb4aub2Deq1TfPgMJPE3x----
Content-Type: text/css
Content-Transfer-Encoding: quoted-printable
Content-Location: cid:css-5afcf630-2125-4dc7-96b8-26f5b199550c@mhtml.blink

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
------MultipartBoundary--jI1qYAMiE8p0qZCDyE3LEZb4aub2Deq1TfPgMJPE3x------
