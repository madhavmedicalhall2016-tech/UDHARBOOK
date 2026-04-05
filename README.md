<!DOCTYPE html>
<html>
<head>
<title>UDHAR BOOK</title>
<style>
body{font-family:Arial;background:#f5f5f5;padding:20px}
.box{background:white;padding:15px;border-radius:10px;max-width:400px;margin:auto}
input,button{width:100%;padding:10px;margin:5px 0}
button{background:green;color:white;border:none}
.list{margin-top:10px}
.item{background:#eee;padding:10px;margin:5px 0}
</style>
</head>
<body>

<div class="box">
<h2>UDHAR BOOK</h2>

<input type="text" id="name" placeholder="Customer Name">
<input type="number" id="amount" placeholder="Amount">
<button onclick="add()">ADD</button>

<div class="list" id="list"></div>
</div>

<script>
function add(){
let name=document.getElementById("name").value;
let amount=document.getElementById("amount").value;

if(name==""||amount=="")return;

let item=document.createElement("div");
item.className="item";
item.innerHTML=name+" : ₹"+amount;

document.getElementById("list").appendChild(item);

document.getElementById("name").value="";
document.getElementById("amount").value="";
}
</script>

</body>
</html>
