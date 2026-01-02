<!DOCTYPE html>
<html>
<head>
  <title>Osmania University Results</title>
  <style>
    body { font-family: Arial; background: #f6f1df; }
    .container { width: 95%; margin: auto; border: 1px solid #999; background: #fffbe6; padding: 10px; }
    h3 { text-align: center; margin: 5px; }
    table { width: 100%; border-collapse: collapse; margin-top: 10px; font-size: 14px; }
    th, td { border: 1px solid #999; padding: 5px; text-align: center; }
    .label { background: #f0d890; font-weight: bold; }
    .btn { padding: 5px 10px; margin-top: 10px; }
    .hidden { display: none; }
  </style>
</head>
<body>
<h3>B.Sc (CBCS) (Regular) III SEM Results</h3>
<div style="text-align:center;">
  Enter Hall Ticket No:
  <input type="text" id="htno">
  <button class="btn" onclick="showResult()">Submit</button>
</div>
<div class="container hidden" id="resultBox">
<table>
  <tr><td class="label">Hall Ticket No</td><td id="r_ht"></td><td class="label">Gender</td><td id="r_gender"></td></tr>
  <tr><td class="label">Name</td><td id="r_name"></td><td class="label">Father's Name</td><td id="r_father"></td></tr>
  <tr><td class="label">Course</td><td id="r_course"></td><td class="label">Medium</td><td id="r_medium"></td></tr>
</table>
<table>
  <tr class="label"><th>Code</th><th>Subject</th><th>Credits</th><th>Grade</th></tr>
  <tr><td>201</td><td>English 2</td><td>4</td><td id="g1"></td></tr>
  <tr><td>205</td><td>Sanskrit 2</td><td>4</td><td id="g2"></td></tr>
  <tr><td>223</td><td>Statistics 2</td><td>4</td><td id="g3"></td></tr>
  <tr><td>281</td><td>Data Science PR</td><td>1</td><td id="g4"></td></tr>
  <tr><td>249</td><td>Mathematics 2</td><td>5</td><td id="g5"></td></tr>
  <tr><td>259A</td><td>Fundamentals of Computer</td><td>2</td><td id="g6"></td></tr>
  <tr><td>280</td><td>Data Science</td><td>4</td><td id="g7"></td></tr>
</table>
<table>
  <tr><td class="label">Semester</td><td>3</td><td class="label">Result</td><td><b>PASS</b></td></tr>
</table>
<p style="font-size:11px;text-align:center;">This is a prank website.</p>
</div>
<script>
const students = {
  "106624459036": {name:"RUPANKH SHASTRY",gender:"MALE",father:"HEMANTH SHASTRY",course:"B.Sc (DS)",medium:"ENGLISH",grades:["A","B+","A","A","B","A","B+"]},
  "106624459037": {name:"AJAY KUMAR",gender:"MALE",father:"RAMESH KUMAR",course:"B.Sc (DS)",medium:"ENGLISH",grades:["B","A","B+","A","A","B","A"]},
  "106624459038": {name:"SNEHA REDDY",gender:"FEMALE",father:"SRINIVAS REDDY",course:"B.Sc (DS)",medium:"ENGLISH",grades:["A","A","A","A","B+","A","A"]}
};
function showResult(){
  const ht=document.getElementById("htno").value;
  const s=students[ht];
  if(!s){ alert("Invalid Hall Ticket Number"); return; }
  document.getElementById("resultBox").classList.remove("hidden");
  r_ht.innerText=ht; r_name.innerText=s.name; r_gender.innerText=s.gender;
  r_father.innerText=s.father; r_course.innerText=s.course; r_medium.innerText=s.medium;
  g1.innerText=s.grades[0]; g2.innerText=s.grades[1]; g3.innerText=s.grades[2];
  g4.innerText=s.grades[3]; g5.innerText=s.grades[4]; g6.innerText=s.grades[5]; g7.innerText=s.grades[6];
}
</script>
</body>
</html>
