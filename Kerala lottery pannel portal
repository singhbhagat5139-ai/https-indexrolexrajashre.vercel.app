<!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Admin Number Panel</title>

<style>
*{
    box-sizing:border-box;
    margin:0;
    padding:0;
}

body{
    font-family:Arial,sans-serif;
    background:#f3f4f6;
    color:#111827;
}

/* LOGIN */
#loginPage{
    min-height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    background:linear-gradient(135deg,#172554,#2563eb);
    padding:20px;
}

.login-box{
    width:100%;
    max-width:380px;
    background:white;
    padding:30px;
    border-radius:16px;
    box-shadow:0 15px 40px #0004;
}

.login-box h1{
    text-align:center;
    margin-bottom:25px;
}

.login-box input{
    width:100%;
    padding:13px;
    margin:8px 0;
    border:1px solid #ddd;
    border-radius:8px;
    font-size:16px;
}

.login-btn{
    width:100%;
    padding:13px;
    margin-top:12px;
    border:0;
    border-radius:8px;
    background:#2563eb;
    color:white;
    font-size:16px;
    cursor:pointer;
}

.error{
    color:#dc2626;
    text-align:center;
    margin-top:10px;
}

/* APP */
#app{
    display:none;
}

.header{
    background:#172554;
    color:white;
    padding:16px 22px;
    display:flex;
    justify-content:space-between;
    align-items:center;
    gap:15px;
}

.header h2{
    font-size:21px;
}

.logout{
    background:#dc2626;
    color:white;
    border:0;
    padding:9px 14px;
    border-radius:7px;
    cursor:pointer;
}

.container{
    max-width:1250px;
    margin:auto;
    padding:20px;
}

/* CARDS */
.cards{
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:15px;
    margin-bottom:20px;
}

.card{
    background:white;
    border-radius:12px;
    padding:20px;
    box-shadow:0 2px 8px #0001;
}

.card p{
    color:#6b7280;
    font-size:14px;
    margin-bottom:8px;
}

.card h2{
    font-size:26px;
}

/* CONTROLS */
.controls{
    background:white;
    padding:18px;
    border-radius:12px;
    margin-bottom:20px;
    box-shadow:0 2px 8px #0001;
}

.controls input,
.controls select{
    padding:11px;
    border:1px solid #ddd;
    border-radius:7px;
    margin:4px;
    font-size:14px;
}

.controls input{
    width:230px;
}

button{
    border:0;
    border-radius:7px;
    padding:11px 15px;
    margin:4px;
    cursor:pointer;
    font-size:14px;
}

.primary{
    background:#2563eb;
    color:white;
}

.success{
    background:#16a34a;
    color:white;
}

.warning{
    background:#f59e0b;
    color:white;
}

.danger{
    background:#dc2626;
    color:white;
}

.dark{
    background:#172554;
    color:white;
}

/* TABLE */
.table-box{
    background:white;
    border-radius:12px;
    overflow:auto;
    box-shadow:0 2px 8px #0001;
}

table{
    width:100%;
    border-collapse:collapse;
    min-width:760px;
}

th,td{
    padding:12px;
    border-bottom:1px solid #e5e7eb;
    text-align:left;
}

th{
    background:#172554;
    color:white;
    position:sticky;
    top:0;
}

.badge{
    background:#dcfce7;
    color:#166534;
    padding:5px 9px;
    border-radius:20px;
    font-size:12px;
}

.badge.inactive{
    background:#fee2e2;
    color:#991b1b;
}

.action-btn{
    padding:7px 10px;
    margin:2px;
}

/* MODAL */
.modal{
    display:none;
    position:fixed;
    inset:0;
    background:#0008;
    justify-content:center;
    align-items:center;
    padding:20px;
    z-index:1000;
}

.modal-box{
    background:white;
    width:100%;
    max-width:420px;
    border-radius:14px;
    padding:25px;
}

.modal-box h2{
    margin-bottom:18px;
}

.modal-box input,
.modal-box select{
    width:100%;
    padding:12px;
    margin:7px 0;
    border:1px solid #ddd;
    border-radius:7px;
}

/* MOBILE */
@media(max-width:900px){
    .cards{
        grid-template-columns:repeat(2,1fr);
    }
}

@media(max-width:600px){

    .header{
        padding:13px;
    }

    .header h2{
        font-size:17px;
    }

    .container{
        padding:12px;
    }

    .cards{
        grid-template-columns:1fr 1fr;
        gap:10px;
    }

    .card{
        padding:14px;
    }

    .card h2{
        font-size:21px;
    }

    .controls input,
    .controls select{
        width:100%;
        margin:5px 0;
    }

    .controls button{
        width:100%;
        margin:5px 0;
    }
}
</style>
</head>

<body>

<!-- LOGIN -->
<div id="loginPage">

    <div class="login-box">

        <h1>🔐 Admin Login</h1>

        <input
            type="text"
            id="username"
            placeholder="Username"
        >

        <input
            type="password"
            id="password"
            placeholder="Password"
        >

        <button class="login-btn" onclick="login()">
            Login
        </button>

        <div id="loginError" class="error"></div>

    </div>

</div>


<!-- MAIN APP -->
<div id="app">

    <div class="header">

        <h2>📊 Number Admin Panel</h2>

        <button class="logout" onclick="logout()">
            Logout
        </button>

    </div>

    <div class="container">

        <!-- DASHBOARD -->
        <div class="cards">

            <div class="card">
                <p>Total Numbers</p>
                <h2 id="totalNumbers">0</h2>
            </div>

            <div class="card">
                <p>Active Numbers</p>
                <h2 id="activeNumbers">0</h2>
            </div>

            <div class="card">
                <p>Price / Number</p>
                <h2>₹149</h2>
            </div>

            <div class="card">
                <p>Total Amount</p>
                <h2 id="totalAmount">₹0</h2>
            </div>

        </div>


        <!-- CONTROLS -->
        <div class="controls">

            <input
                type="text"
                id="search"
                placeholder="🔎 Number या Name खोजें"
                oninput="applyFilter()"
            >

            <select
                id="statusFilter"
                onchange="applyFilter()"
            >
                <option value="all">सभी Status</option>
                <option value="Active">Active</option>
                <option value="Inactive">Inactive</option>
            </select>

            <button
                class="primary"
                onclick="generate1000()"
            >
                🔢 Generate 1000
            </button>

            <button
                class="success"
                onclick="openAddModal()"
            >
                ➕ Add Number
            </button>

            <button
                class="dark"
                onclick="downloadCSV()"
            >
                📥 CSV / Excel
            </button>

            <button
                class="danger"
                onclick="deleteAll()"
            >
                🗑️ Delete All
            </button>

        </div>


        <!-- TABLE -->
        <div class="table-box">

            <table>

                <thead>
                    <tr>
                        <th>#</th>
                        <th>Number</th>
                        <th>Name</th>
                        <th>Amount</th>
                        <th>Status</th>
                        <th>Action</th>
                    </tr>
                </thead>

                <tbody id="tableBody"></tbody>

            </table>

        </div>

    </div>

</div>


<!-- ADD / EDIT MODAL -->
<div class="modal" id="modal">

    <div class="modal-box">

        <h2 id="modalTitle">Add Number</h2>

        <input
            type="text"
            id="numberInput"
            placeholder="Number"
        >

        <input
            type="text"
            id="nameInput"
            placeholder="Name"
        >

        <input
            type="number"
            id="amountInput"
            value="149"
            placeholder="Amount"
        >

        <select id="statusInput">
            <option value="Active">Active</option>
            <option value="Inactive">Inactive</option>
        </select>

        <button
            class="success"
            onclick="saveNumber()"
        >
            💾 Save
        </button>

        <button
            class="danger"
            onclick="closeModal()"
        >
            Cancel
        </button>

    </div>

</div>


<script>

/* =========================
   LOGIN
========================= */

const ADMIN_USERNAME = "raja";
const ADMIN_PASSWORD = "raja@#8990";

function login(){

    const username =
        document.getElementById("username").value.trim();

    const password =
        document.getElementById("password").value;

    if(
        username === ADMIN_USERNAME &&
        password === ADMIN_PASSWORD
    ){

        localStorage.setItem("adminLoggedIn","true");

        document.getElementById("loginPage").style.display="none";
        document.getElementById("app").style.display="block";

        document.getElementById("loginError").innerText="";

        render();

    }else{

        document.getElementById("loginError").innerText =
            "❌ Username या Password गलत है";

    }
}


function logout(){

    localStorage.removeItem("adminLoggedIn");

    document.getElementById("app").style.display="none";
    document.getElementById("loginPage").style.display="flex";

}


/* =========================
   DATA
========================= */

let numbers =
    JSON.parse(localStorage.getItem("numberData") || "[]");

let editIndex = -1;


/* =========================
   GENERATE 1000
========================= */

function generate1000(){

    if(numbers.length > 0){

        const confirmGenerate =
            confirm(
                "पुराना data मौजूद है। क्या फिर से 1000 नंबर generate करना है?"
            );

        if(!confirmGenerate) return;
    }

    numbers = [];

    const used = new Set();

    while(numbers.length < 1000){

        let num =
            Math.floor(100000 + Math.random() * 900000)
            .toString();

        if(!used.has(num)){

            used.add(num);

            numbers.push({
                number:"KL " + num,
                name:"Kundan Kumar",
                amount:149,
                status:"Active"
            });

        }
    }

    saveData();
    render();

    alert("✅ 1000 नंबर successfully generate हो गए।");
}


/* =========================
   ADD
========================= */

function openAddModal(){

    editIndex = -1;

    document.getElementById("modalTitle").innerText =
        "Add Number";

    document.getElementById("numberInput").value="";
    document.getElementById("nameInput").value="";
    document.getElementById("amountInput").value=149;
    document.getElementById("statusInput").value="Active";

    document.getElementById("modal").style.display="flex";
}


function closeModal(){

    document.getElementById("modal").style.display="none";

}


/* =========================
   SAVE / EDIT
========================= */

function saveNumber(){

    const number =
        document.getElementById("numberInput").value.trim();

    const name =
        document.getElementById("nameInput").value.trim();

    const amount =
        Number(document.getElementById("amountInput").value) || 0;

    const status =
        document.getElementById("statusInput").value;

    if(!number){

        alert("कृपया Number डालें।");
        return;

    }

    if(editIndex === -1){

        numbers.push({
            number:number,
            name:name || "-",
            amount:amount,
            status:status
        });

    }else{

        numbers[editIndex] = {
            number:number,
            name:name || "-",
            amount:amount,
            status:status
        };

    }

    saveData();
    closeModal();
    render();

}


/* =========================
   EDIT
========================= */

function editNumber(index){

    editIndex = index;

    const item = numbers[index];

    document.getElementById("modalTitle").innerText =
        "Edit Number";

    document.getElementById("numberInput").value =
        item.number;

    document.getElementById("nameInput").value =
        item.name;

    document.getElementById("amountInput").value =
        item.amount;

    document.getElementById("statusInput").value =
        item.status;

    document.getElementById("modal").style.display="flex";

}


/* =========================
   DELETE
========================= */

function deleteNumber(index){

    if(
        confirm(
            "क्या आप इस नंबर को delete करना चाहते हैं?"
        )
    ){

        numbers.splice(index,1);

        saveData();
        render();

    }

}


function deleteAll(){

    if(numbers.length === 0){

        alert("Delete करने के लिए कोई data नहीं है।");
        return;

    }

    if(
        confirm(
            "⚠️ क्या आप सभी नंबर delete करना चाहते हैं?"
        )
    ){

        numbers = [];

        saveData();
        render();

    }

}


/* =========================
   FILTER
========================= */

function applyFilter(){

    render();

}


/* =========================
   RENDER TABLE
========================= */

function render(){

    const tbody =
        document.getElementById("tableBody");

    const search =
        document.getElementById("search").value
        .toLowerCase()
        .trim();

    const status =
        document.getElementById("statusFilter").value;

    tbody.innerHTML="";

    let filtered = numbers.filter(item => {

        const matchesSearch =
            item.number.toLowerCase().includes(search) ||
            item.name.toLowerCase().includes(search);

        const matchesStatus =
            status === "all" ||
            item.status === status;

        return matchesSearch && matchesStatus;

    });


    filtered.forEach(item => {

        const realIndex =
            numbers.indexOf(item);

        const tr =
            document.createElement("tr");

        tr.innerHTML = `

            <td>${realIndex + 1}</td>

            <td>
                <strong>${escapeHTML(item.number)}</strong>
            </td>

            <td>
                ${escapeHTML(item.name)}
            </td>

            <td>
                ₹${Number(item.amount).toLocaleString("en-IN")}
            </td>

            <td>

                <span class="badge ${
                    item.status === "Inactive"
                    ? "inactive"
                    : ""
                }">

                    ${item.status}

                </span>

            </td>

            <td>

                <button
                    class="warning action-btn"
                    onclick="editNumber(${realIndex})"
                >
                    ✏️ Edit
                </button>

                <button
                    class="danger action-btn"
                    onclick="deleteNumber(${realIndex})"
                >
                    🗑️ Delete
                </button>

            </td>

        `;

        tbody.appendChild(tr);

    });


    updateDashboard();

}


/* =========================
   DASHBOARD
========================= */

function updateDashboard(){

    const total =
        numbers.length;

    const active =
        numbers.filter(
            item => item.status === "Active"
        ).length;

    const amount =
        numbers.reduce(
            (sum,item) =>
                sum + Number(item.amount || 0),
            0
        );


    document.getElementById("totalNumbers")
        .innerText = total;

    document.getElementById("activeNumbers")
        .innerText = active;

    document.getElementById("totalAmount")
        .innerText =
        "₹" + amount.toLocaleString("en-IN");

}


/* =========================
   CSV DOWNLOAD
========================= */

function downloadCSV(){

    if(numbers.length === 0){

        alert("Download करने के लिए data नहीं है।");
        return;

    }

    let csv =
        "S.No,Number,Name,Amount,Status\n";

    numbers.forEach((item,index)=>{

        csv +=
            `${index+1},"${item.number.replace(/"/g,'""')}","${item.name.replace(/"/g,'""')}",${item.amount},"${item.status}"\n`;

    });


    const blob =
        new Blob(
            ["\ufeff" + csv],
            {
                type:"text/csv;charset=utf-8;"
            }
        );

    const url =
        URL.createObjectURL(blob);

    const link =
        document.createElement("a");

    link.href = url;

    link.download =
        "number-data.csv";

    document.body.appendChild(link);

    link.click();

    document.body.removeChild(link);

    URL.revokeObjectURL(url);

}


/* =========================
   SAVE DATA
========================= */

function saveData(){

    localStorage.setItem(
        "numberData",
        JSON.stringify(numbers)
    );

}


/* =========================
   SECURITY / HTML ESCAPE
========================= */

function escapeHTML(value){

    return String(value)
        .replace(/&/g,"&amp;")
        .replace(/</g,"&lt;")
        .replace(/>/g,"&gt;")
        .replace(/"/g,"&quot;")
        .replace(/'/g,"&#039;");

}


/* =========================
   AUTO LOGIN CHECK
========================= */

window.onload = function(){

    if(
        localStorage.getItem("adminLoggedIn") === "true"
    ){

        document.getElementById("loginPage").style.display="none";
        document.getElementById("app").style.display="block";

    }

    render();

};

</script>

</body>
</html>
