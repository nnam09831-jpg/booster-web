<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Booster Pro</title>

<style>
body{
    background:#0f172a;
    color:white;
    font-family:Arial;
    text-align:center;
    margin:0;
}

.container{
    max-width:450px;
    margin:auto;
    padding:20px;
}

.card{
    background:#1e293b;
    border-radius:15px;
    padding:20px;
    margin-top:15px;
}

input{
    width:90%;
    padding:10px;
    border:none;
    border-radius:8px;
}

button{
    padding:10px 20px;
    margin-top:10px;
    border:none;
    border-radius:8px;
    cursor:pointer;
}

.switch{
    display:flex;
    justify-content:space-between;
    margin:12px 0;
}

.status{
    color:#00ff88;
}
</style>
</head>

<body>

<div class="container">

<h1>🚀 BOOSTER PRO</h1>

<div class="card">
<h3>👤 Admin: Nguyễn Nam</h3>

<input id="keyInput" placeholder="Nhập key">
<br>
<button onclick="login()">Kích hoạt</button>

<p id="loginStatus">🔒 Chưa kích hoạt</p>
</div>

<div class="card" id="panel" style="display:none">

<h3>⚙️ Chức năng</h3>

<div class="switch">
<span>Boost Mode</span>
<input type="checkbox">
</div>

<div class="switch">
<span>Game Mode</span>
<input type="checkbox">
</div>

<div class="switch">
<span>FPS Monitor</span>
<input type="checkbox">
</div>

<div class="switch">
<span>Network Check</span>
<input type="checkbox">
</div>

<div class="switch">
<span>Battery Saver</span>
<input type="checkbox">
</div>

<p class="status">✅ Hệ thống đã sẵn sàng</p>

</div>

</div>

<script>
const VALID_KEY = "NGUYENNAM2026";

function login(){
    const key =
    document.getElementById("keyInput").value;

    if(key === VALID_KEY){
        document.getElementById("loginStatus")
        .innerHTML="✅ Kích hoạt thành công";

        document.getElementById("panel")
        .style.display="block";
    }else{
        alert("Key không hợp lệ");
    }
}
</script>

</body>
</html>
