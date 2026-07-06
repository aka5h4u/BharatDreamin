<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Educators For Good</title>

<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Inter',sans-serif;
}

body{
background:#f6f8fb;
color:#222;
}

header{
background:white;
padding:20px 60px;
display:flex;
justify-content:space-between;
align-items:center;
box-shadow:0 2px 12px rgba(0,0,0,.05);
position:sticky;
top:0;
}

.logo{
font-size:28px;
font-weight:700;
color:#0176D3;
}

nav a{
margin-left:30px;
text-decoration:none;
color:#444;
font-weight:500;
}

.hero{
display:flex;
justify-content:space-between;
align-items:center;
padding:80px;
}

.hero-text{
width:55%;
}

.hero h1{
font-size:58px;
line-height:1.2;
margin-bottom:20px;
}

.hero p{
font-size:20px;
color:#666;
margin-bottom:35px;
}

button{
padding:16px 28px;
border:none;
border-radius:10px;
font-size:16px;
cursor:pointer;
margin-right:15px;
}

.primary{
background:#0176D3;
color:white;
}

.secondary{
background:white;
border:2px solid #0176D3;
color:#0176D3;
}

.hero-card{
width:360px;
background:white;
padding:30px;
border-radius:20px;
box-shadow:0 20px 40px rgba(0,0,0,.08);
}

.hero-card h3{
margin-bottom:15px;
color:#0176D3;
}

.stats{
display:grid;
grid-template-columns:repeat(3,1fr);
gap:25px;
padding:50px 80px;
}

.stat{
background:white;
padding:30px;
border-radius:15px;
text-align:center;
box-shadow:0 5px 15px rgba(0,0,0,.05);
}

.stat h2{
color:#0176D3;
margin-bottom:10px;
}

.section{
padding:70px 80px;
}

.cards{
display:grid;
grid-template-columns:repeat(3,1fr);
gap:25px;
margin-top:30px;
}

.card{
background:white;
padding:25px;
border-radius:15px;
box-shadow:0 10px 25px rgba(0,0,0,.05);
}

.card h3{
margin-bottom:15px;
color:#0176D3;
}

.chat{
position:fixed;
right:30px;
bottom:30px;
width:370px;
background:white;
border-radius:20px;
box-shadow:0 15px 50px rgba(0,0,0,.25);
overflow:hidden;
}

.chat-header{
background:#0176D3;
color:white;
padding:18px;
font-size:18px;
font-weight:600;
}

.chat-body{
padding:18px;
height:340px;
overflow:auto;
background:#f9fbff;
}

.message{
margin-bottom:15px;
padding:12px 15px;
border-radius:12px;
max-width:90%;
}

.bot{
background:white;
}

.user{
background:#0176D3;
color:white;
margin-left:auto;
}

.chat-footer{
padding:15px;
display:flex;
gap:10px;
}

.chat-footer input{
flex:1;
padding:12px;
border-radius:8px;
border:1px solid #ddd;
}

.chat-footer button{
background:#0176D3;
color:white;
padding:12px 18px;
margin:0;
}

.footer{
padding:40px;
text-align:center;
color:#777;
}

</style>
</head>

<body>

<header>

<div class="logo">
Educators For Good
</div>

<nav>

<a href="#">Home</a>
<a href="#">Programs</a>
<a href="#">Grants</a>
<a href="#">Impact</a>
<a href="#">Contact</a>

</nav>

</header>

<section class="hero">

<div class="hero-text">

<h1>
Empowering Education Through Smart Grant Management
</h1>

<p>
Helping nonprofits discover funding opportunities, manage grants, and measure impact using Salesforce Agentforce.
</p>

<button class="primary">
Find Grants
</button>

<button class="secondary">
Our Impact
</button>

</div>

<div class="hero-card">

<h3>Grant Overview</h3>

<p><strong>Open Opportunities</strong></p>
<h2>27</h2>

<br>

<p><strong>Funds Awarded</strong></p>
<h2>₹8.2 Crore</h2>

<br>

<p><strong>Projects Supported</strong></p>
<h2>146</h2>

</div>

</section>

<section class="stats">

<div class="stat">
<h2>8,450</h2>
<p>Students Impacted</p>
</div>

<div class="stat">
<h2>312</h2>
<p>Schools Supported</p>
</div>

<div class="stat">
<h2>95%</h2>
<p>Grant Success Rate</p>
</div>

</section>

<section class="section">

<h2>Available Funding Opportunities</h2>

<div class="cards">

<div class="card">

<h3>Education Innovation Grant</h3>

<p>Amount</p>

<h2>₹50 Lakhs</h2>

<br>

<p>Eligibility Score</p>

<h3>98%</h3>

</div>

<div class="card">

<h3>Digital Classroom Grant</h3>

<p>Amount</p>

<h2>₹25 Lakhs</h2>

<br>

<p>Eligibility Score</p>

<h3>91%</h3>

</div>

<div class="card">

<h3>Girls Education Initiative</h3>

<p>Amount</p>

<h2>₹35 Lakhs</h2>

<br>

<p>Eligibility Score</p>

<h3>94%</h3>

</div>

</div>

</section>

<div class="chat">

<div class="chat-header">

🤖 Agentforce Grant Assistant

</div>

<div class="chat-body" id="chat">

<div class="message bot">

👋 Hello!

I'm your Grant Assistant.

Tell me about your organization and I'll help you:

✅ Find grants

✅ Check eligibility

✅ Start an application

</div>

</div>

<div class="chat-footer">

<input
id="message"
placeholder="Type your question..."
>

<button onclick="send()">
Send
</button>

</div>

</div>

<div class="footer">

Powered by Salesforce Agentforce • Demo Homepage

</div>

<script>

function send(){

let input=document.getElementById("message");

if(input.value=="") return;

let chat=document.getElementById("chat");

chat.innerHTML+=`
<div class="message user">
${input.value}
</div>
`;

setTimeout(function(){

chat.innerHTML+=`

<div class="message bot">

Based on your organization's profile, I found two grants that match your mission.

✅ Education Innovation Grant

Match Score: 98%

Funding: ₹50 Lakhs

Deadline: 20 Aug 2026

<br><br>

Would you like me to check your eligibility and pre-fill the application?

</div>

`;

chat.scrollTop=chat.scrollHeight;

},700);

input.value="";

chat.scrollTop=chat.scrollHeight;

}

</script>

</body>
</html>
