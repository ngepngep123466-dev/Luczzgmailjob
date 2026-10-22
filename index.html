<!doctype html>
<html lang="id">
<head>
<meta charset="utf-8"><meta name="viewport" content="width=device-width,initial-scale=1">
<meta name="theme-color" content="#10091d"><title>Luczz Gmail</title>
<style>
:root{--bg:#0b0712;--panel:#171024;--line:#493064;--pink:#ff43ce;--violet:#9e65ff;--text:#f7efff;--muted:#bdaecc;--green:#64efb2}
*{box-sizing:border-box}body{margin:0;background:radial-gradient(ellipse at top,#2c1248,var(--bg) 60%);color:var(--text);font:15px system-ui,Arial,sans-serif}
header{position:sticky;top:0;z-index:2;background:#10091dee;border-bottom:1px solid var(--line);padding:14px 16px;display:flex;align-items:center;justify-content:space-between;gap:10px}
.brand{font-size:23px;font-weight:900;letter-spacing:-.8px;background:linear-gradient(90deg,#fff,var(--pink),var(--violet));background-clip:text;color:transparent}
main{max-width:1000px;margin:20px auto;padding:0 12px 40px}.panel{background:#171024f5;border:1px solid var(--line);border-radius:15px;padding:16px;margin:12px 0;box-shadow:0 8px 25px #0002}
h2,h3{margin:0 0 12px}p{line-height:1.5}.muted,small{color:var(--muted)}.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(min(100%,280px),1fr));gap:10px}
input,textarea,select{display:block;width:100%;padding:12px;margin:6px 0 12px;border-radius:9px;border:1px solid #5a3d75;background:#0d0815;color:#fff;font:inherit}textarea{min-height:125px;resize:vertical}
button{border:0;border-radius:9px;padding:11px 14px;margin:3px 3px 3px 0;background:linear-gradient(100deg,#9c45ff,#ed43cb);color:white;font-weight:750;font-size:14px;cursor:pointer}button.secondary{background:#30223f;border:1px solid #60477a}button.danger{background:#9e2c50}button:disabled{opacity:.45}
.tabs{display:flex;gap:7px;flex-wrap:wrap}.hidden{display:none!important}.row{border-top:1px solid var(--line);padding:10px 0;overflow-wrap:anywhere}.pill{border:1px solid var(--line);border-radius:99px;padding:5px 9px;color:#e1ceff;font-size:12px}.good{color:var(--green)}.bad{color:#ff8cae}.notice{padding:10px;border-radius:9px;background:#241533;margin:10px 0;overflow-wrap:anywhere}
.wa{display:flex;align-items:center;gap:12px;text-decoration:none;color:white;padding:12px;border:1px solid #2d7956;border-radius:12px;background:#0c241b}.wa svg{width:42px;height:42px;flex-shrink:0}.tiny{font-size:12px}.actions{display:flex;gap:6px;flex-wrap:wrap}.total{font-weight:800;color:#f4c4ff}
@media(max-width:480px){.brand{font-size:20px}header{padding:12px}.panel{padding:13px}main{padding:0 9px 30px}}
</style></head>
<body><header><div class="brand">Luczz Gmail</div><div id="head"></div></header><main><div id="app"></div><p class="muted tiny">Gunakan hanya alamat email yang kamu miliki atau berwenang kelola. Jangan masukkan password email, OTP, atau kode pemulihan.</p></main>
<script>
/*
  HTML-ONLY LOCAL VERSION:
  Data tersimpan di localStorage pada browser/perangkat ini saja.
  Bukan autentikasi server dan tidak sinkron antar perangkat/user.
  Jangan gunakan untuk mengelola uang atau data nyata sebelum memasang backend.
*/
const KEY="luczz_gmail_html_v1";
const initial={users:[],inventory:[],bookings:[],submissions:[],withdrawals:[],settings:{
 booking_enabled:false,booking_title:"Booking Gmail",booking_description:"Booking hanya untuk alamat email yang owner berwenang kelola.",
 stor_title:"Stor",stor_description:"Masukkan alamat email satu per baris untuk ditinjau owner.",
 announcement:"Jangan masukkan password, OTP, atau kode pemulihan.",
 whatsapp_url:"https://whatsapp.com/channel/0029Vb8sNmqFXUuVvXyWBW2W"
}};
let db=load(),me=null;
function load(){try{return JSON.parse(localStorage.getItem(KEY))||structuredClone(initial)}catch{return structuredClone(initial)}}
function save(){localStorage.setItem(KEY,JSON.stringify(db))}
const $=s=>document.querySelector(s);
function esc(s){return String(s??"").replace(/[&<>"']/g,c=>({"&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;","'":"&#39;"}[c]))}
function id(){return Date.now().toString(36)+Math.random().toString(36).slice(2,8)}
function money(n){return Number(n||0).toLocaleString("id-ID")}
function alertMsg(s,good=false){let n=$("#notice");if(n)n.innerHTML=`<div class="notice ${good?"good":"bad"}">${esc(s)}</div>`;else alert(s)}
function authScreen(tab="login"){
 me=null;$("#head").innerHTML="";$("#app").innerHTML=`<section class="panel" style="max-width:470px;margin:32px auto"><h2>${tab==="login"?"Login":"Daftar"} Luczz Gmail</h2><div class="tabs"><button class="${tab==="login"?"":"secondary"}" onclick="authScreen('login')">Login</button><button class="${tab==="register"?"":"secondary"}" onclick="authScreen('register')">Daftar</button></div><form id="auth"><label>Username</label><input name="username" required minlength="3" autocomplete="username"><label>Password</label><input name="password" type="password" required minlength="6" autocomplete="${tab==="login"?"current-password":"new-password"}">${tab==="register"?'<label>Nomor WhatsApp</label><input name="wa" required minlength="8" placeholder="08xxxxxxxxxx">':''}<button>${tab==="login"?"Masuk":"Buat akun"}</button></form><div id="notice"></div><p class="muted tiny">Catatan: versi HTML menyimpan data di browser HP ini. Login tidak tersinkron ke perangkat lain.</p></section>`;
 $("#auth").onsubmit=e=>{e.preventDefault();let f=Object.fromEntries(new FormData(e.target));if(tab==="register"){if(db.users.some(u=>u.username.toLowerCase()===f.username.toLowerCase()))return alertMsg("Username sudah digunakan.");let u={id:id(),username:f.username,password:f.password,wa:f.wa,role:"user",balance:0,banned:false};db.users.push(u);save();me=u;render();return}
 let u=f.username==="ambatukam"&&f.password==="123456p"?{id:"owner",username:"ambatukam",role:"owner",balance:0,wa:"-"}:db.users.find(u=>u.username===f.username&&u.password===f.password);
 if(!u)return alertMsg("Username atau password salah.");if(u.banned)return alertMsg("Akun diblokir owner.");me=u;render();
 };
}
function shell(content){$("#head").innerHTML=me?`<span class="pill">${esc(me.username)} · ${esc(me.role)}</span> <button class="secondary" onclick="logout()">Keluar</button>`:"";$("#app").innerHTML=content}
function logout(){me=null;authScreen()}
function render(){if(me.role==="owner")ownerView();else userView()}
function userView(){
 let myB=db.bookings.filter(x=>x.user===me.id),myS=db.submissions.filter(x=>x.user===me.id),myW=db.withdrawals.filter(x=>x.user===me.id);
 let available=db.inventory.filter(x=>!x.bookedBy).length,availableStatus=db.settings.booking_enabled&&available>0?"tersedia":"tidak tersedia";
 shell(`<h2>Dashboard User</h2><div id="notice"></div><div class="grid"><section class="panel"><h3>Saldo</h3><h2>Rp ${money(me.balance)}</h2><small>Saldo bertambah setelah Stor disetujui owner.</small></section><section class="panel"><h3>${esc(db.settings.booking_title)}</h3><p>${esc(db.settings.booking_description)}</p><p>Status booking: <b>${availableStatus}</b></p><form id="bookForm"><label>Jumlah (1–100.000)</label><input name="n" type="number" min="1" max="100000" value="1" required><button ${availableStatus!=="tersedia"?"disabled":""}>Booking</button></form><div id="bookResult"></div></section></div>
<section class="panel"><h3>${esc(db.settings.stor_title)}</h3><p>${esc(db.settings.stor_description)}</p><form id="storForm"><label>Alamat email, satu per baris</label><textarea name="emails" required placeholder="contoh1@example.com&#10;contoh2@example.com"></textarea><p class="muted">Rp2.500 per alamat yang disetujui.</p><p id="estimate" class="total">Perkiraan: Rp0</p><button>Kirim Stor</button></form></section>
<div class="grid"><section class="panel"><h3>Penarikan saldo</h3><form id="withdrawForm"><label>Nominal</label><input name="amount" type="number" min="1" required><label>Metode</label><select name="method"><option>DANA</option><option>GoPay</option><option>OVO</option></select><label>Nomor tujuan</label><input name="destination" required><button>Ajukan penarikan</button></form><small>Jika ditolak, saldo akan dikembalikan (di browser ini).</small></section><section class="panel"><h3>Saluran WhatsApp</h3><a class="wa" href="${esc(db.settings.whatsapp_url)}" target="_blank" rel="noopener"><svg viewBox="0 0 32 32" fill="#25D366" aria-label="WhatsApp"><path d="M16 .8A15 15 0 0 0 3.1 23.5L1 31l7.7-2A15 15 0 1 0 16 .8Zm0 27.4a12.3 12.3 0 0 1-6.3-1.7l-.5-.3-4.6 1.2 1.2-4.5-.3-.5A12.3 12.3 0 1 1 16 28.2Zm6.8-9.2c-.4-.2-2.3-1.1-2.7-1.2-.4-.1-.6-.2-.9.2-.3.4-1 1.2-1.2 1.4-.2.3-.5.3-.9.1-.4-.2-1.7-.6-3.2-2-1.2-1.1-2-2.4-2.2-2.8-.2-.4 0-.6.2-.8l.6-.7c.2-.2.3-.4.4-.7.1-.3 0-.5 0-.7-.1-.2-.9-2.1-1.3-2.9-.3-.7-.7-.6-.9-.6h-.8c-.3 0-.7.1-1.1.5-.4.4-1.4 1.4-1.4 3.3s1.4 3.8 1.6 4.1c.2.3 2.8 4.3 6.8 6 .9.4 1.6.6 2.1.7.9.3 1.8.2 2.4.1.7-.1 2.3-.9 2.6-1.9.3-.9.3-1.7.2-1.9-.1-.2-.4-.3-.8-.5Z"/></svg><b>Saluran WhatsApp</b></a></section></div>
<div class="grid"><section class="panel"><h3>Booking saya</h3>${myB.map(x=>`<div class="row">${esc(x.email)} <button class="secondary" onclick="copyEmail('${esc(x.email)}')">Salin</button><p class="muted tiny">Wajib digunakan untuk Stor terkait. Disimpan pada browser ini.</p></div>`).join("")||"<small>Belum ada booking.</small>"}</section><section class="panel"><h3>Riwayat Stor</h3>${myS.map(x=>`<div class="row">${esc(x.email)} · ${esc(x.status)} · Rp ${money(x.amount)}</div>`).join("")||"<small>Belum ada Stor.</small>"}</section><section class="panel"><h3>Riwayat penarikan</h3>${myW.map(x=>`<div class="row">Rp ${money(x.amount)} · ${esc(x.method)} · ${esc(x.status)}</div>`).join("")||"<small>Belum ada permintaan.</small>"}</section><section class="panel"><h3>Data akun</h3><p>Username: ${esc(me.username)}</p><p>Role: user</p><p>WhatsApp: ${esc(me.wa)}</p></section></div>`);
 let ta=$("#storForm textarea");ta.oninput=()=>{let a=[...new Set(ta.value.split(/\r?\n/).map(s=>s.trim()).filter(Boolean))];$("#estimate").textContent=`Perkiraan jika disetujui: Rp ${money(a.length*2500)} (${a.length} alamat)`};
 $("#bookForm").onsubmit=e=>{e.preventDefault();let n=Number(new FormData(e.target).get("n")),stock=db.inventory.filter(x=>!x.bookedBy);if(!Number.isInteger(n)||n<1||n>100000)return alertMsg("Jumlah harus 1–100.000.");if(!db.settings.booking_enabled)return alertMsg("Booking sedang OFF.");if(stock.length<n)return alertMsg("Stok tidak mencukupi. Tersedia "+stock.length+".");let picked=stock.slice(0,n);picked.forEach(x=>{x.bookedBy=me.id;db.bookings.push({id:id(),user:me.id,email:x.email,created:new Date().toISOString()})});save();userView();$("#bookResult")?.replaceChildren();};
 $("#storForm").onsubmit=e=>{e.preventDefault();let arr=[...new Set(new FormData(e.target).get("emails").split(/\r?\n/).map(s=>s.trim()).filter(Boolean))];if(!arr.length)return;let invalid=arr.find(x=>!/^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(x));if(invalid)return alertMsg("Format alamat tidak valid: "+invalid);const bookedEmails=new Set(db.bookings.filter(b=>b.user===me.id).map(b=>b.email.toLowerCase()));
let notBooked=arr.filter(email=>!bookedEmails.has(email.toLowerCase()));
if(notBooked.length)return alertMsg("Stor hanya boleh memakai alamat yang kamu booking. Belum dibooking: "+notBooked.join(", "));
let alreadyPending=arr.filter(email=>db.submissions.some(x=>x.user===me.id&&x.email.toLowerCase()===email.toLowerCase()&&x.status==="pending"));
if(alreadyPending.length)return alertMsg("Alamat ini masih menunggu pemeriksaan: "+alreadyPending.join(", "));
arr.forEach(email=>db.submissions.push({id:id(),user:me.id,email,status:"pending",amount:0}));save();alertMsg(`Stor terkirim: ${arr.length} alamat. Perkiraan Rp ${money(arr.length*2500)}; menunggu pemeriksaan owner. Booking akan hilang setelah disetujui owner.`,true);userView()};
 $("#withdrawForm").onsubmit=e=>{e.preventDefault();let f=Object.fromEntries(new FormData(e.target)),amount=Number(f.amount);if(!Number.isSafeInteger(amount)||amount<1)return alertMsg("Nominal tidak valid.");if(amount>me.balance)return alertMsg("Saldo tidak mencukupi.");me.balance-=amount;db.withdrawals.push({id:id(),user:me.id,amount,method:f.method,destination:f.destination,status:"pending"});save();userView();alertMsg("Permintaan penarikan dikirim. Saldo ditahan.",true)};
}
function copyEmail(s){if(navigator.clipboard)navigator.clipboard.writeText(s).then(()=>alert("Alamat disalin")).catch(()=>prompt("Salin alamat ini:",s));else prompt("Salin alamat ini:",s)}
function ownerView(){
 let pending=db.submissions.filter(x=>x.status==="pending"),pw=db.withdrawals.filter(x=>x.status==="pending");
 shell(`<h2>Dashboard Owner</h2><div id="notice"></div><div class="grid"><section class="panel"><h3>Pengaturan tampilan</h3><form id="settingsForm"><label>Judul Booking</label><input name="booking_title" value="${esc(db.settings.booking_title)}"><label>Deskripsi Booking</label><textarea name="booking_description">${esc(db.settings.booking_description)}</textarea><label>Booking</label><select name="booking_enabled"><option value="true" ${db.settings.booking_enabled?"selected":""}>ON</option><option value="false" ${!db.settings.booking_enabled?"selected":""}>OFF</option></select><label>Judul Stor</label><input name="stor_title" value="${esc(db.settings.stor_title)}"><label>Deskripsi Stor</label><textarea name="stor_description">${esc(db.settings.stor_description)}</textarea><label>Pengumuman</label><textarea name="announcement">${esc(db.settings.announcement)}</textarea><button>Simpan</button></form></section><section class="panel"><h3>Tambah stok Booking</h3><p class="muted">Satu email per baris. Item hanya bisa dibooking sekali pada browser ini.</p><form id="inventoryForm"><textarea name="emails" required placeholder="email1@example.com&#10;email2@example.com"></textarea><button>Tambah stok</button></form><p>Stok tersedia: ${db.inventory.filter(x=>!x.bookedBy).length}</p><p>User terdaftar: ${db.users.length}</p><button class="secondary" onclick="exportData()">Ekspor cadangan JSON</button><label class="tiny">Impor cadangan JSON</label><input type="file" id="importFile" accept=".json,application/json"></section></div>
<section class="panel"><h3>Hasil Stor / Pending (${pending.length})</h3>${db.submissions.map(x=>{let u=db.users.find(u=>u.id===x.user);return `<div class="row">${esc(u?.username||"user")} · ${esc(x.email)} · <b>${esc(x.status)}</b> ${x.status==="pending"?`<button onclick="reviewStor('${x.id}',true)">Terima (+Rp2.500)</button><button class="danger" onclick="reviewStor('${x.id}',false)">Tolak</button>`:""} </div>`}).join("")||"<small>Belum ada Stor.</small>"}</section>
<section class="panel"><h3>Permintaan penarikan (${pw.length})</h3>${db.withdrawals.map(x=>{let u=db.users.find(u=>u.id===x.user);return `<div class="row">${esc(u?.username)} · Rp ${money(x.amount)} · ${esc(x.method)} ${esc(x.destination)} · <b>${esc(x.status)}</b> ${x.status==="pending"?`<button onclick="reviewWithdrawal('${x.id}',true)">Setujui</button><button class="danger" onclick="reviewWithdrawal('${x.id}',false)">Tolak & kembalikan saldo</button>`:""}</div>`}).join("")||"<small>Belum ada permintaan.</small>"}</section>
<div class="grid"><section class="panel"><h3>Data akun user</h3>${db.users.map(u=>`<div class="row"><b>${esc(u.username)}</b> · role user · WA ${esc(u.wa)} · saldo Rp ${money(u.balance)} · ${u.banned?"DIBLOKIR":"aktif"}<br><button class="danger" onclick="toggleBan('${u.id}')">${u.banned?"Buka blokir":"Blokir user"}</button></div>`).join("")||"<small>Belum ada user.</small>"}</section><section class="panel"><h3>Stok dan booking</h3>${db.inventory.map(x=>`<div class="row">${esc(x.email)} · ${x.bookedBy?"dibooking oleh "+esc(db.users.find(u=>u.id===x.bookedBy)?.username||"user"):"tersedia"}</div>`).join("")||"<small>Stok kosong.</small>"}</section></div>`);
 $("#settingsForm").onsubmit=e=>{e.preventDefault();let f=Object.fromEntries(new FormData(e.target));Object.assign(db.settings,f,{booking_enabled:f.booking_enabled==="true"});save();ownerView();alertMsg("Pengaturan tersimpan.",true)};
 $("#inventoryForm").onsubmit=e=>{e.preventDefault();let arr=[...new Set(new FormData(e.target).get("emails").split(/\r?\n/).map(s=>s.trim()).filter(Boolean))];if(arr.some(x=>!/^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(x)))return alertMsg("Ada alamat yang formatnya tidak valid.");let added=0;arr.forEach(email=>{if(!db.inventory.some(x=>x.email.toLowerCase()===email.toLowerCase())){db.inventory.push({id:id(),email,bookedBy:null});added++}});save();ownerView();alertMsg(added+" alamat baru ditambahkan.",true)};
 $("#importFile").onchange=async e=>{let f=e.target.files[0];if(!f)return;try{let d=JSON.parse(await f.text());if(!d.users||!d.inventory||!d.settings)throw Error("Format cadangan tidak sesuai.");if(confirm("Mengganti data lokal saat ini dengan cadangan ini?")){db=d;save();ownerView();alertMsg("Cadangan diimpor.",true)}}catch(err){alertMsg("Impor gagal: "+err.message)}};
}
function reviewStor(id,approve){
 let x=db.submissions.find(x=>x.id===id&&x.status==="pending");if(!x)return;
 let u=db.users.find(u=>u.id===x.user);
 x.status=approve?"approved":"rejected";x.amount=approve?2500:0;
 // Booking terkait selalu dihapus setelah Stor diputuskan, baik diterima maupun ditolak.
 const emailKey=x.email.toLowerCase();
 const booking=db.bookings.find(b=>b.user===x.user&&b.email.toLowerCase()===emailKey);
 if(booking){
   db.bookings=db.bookings.filter(b=>!(b.user===x.user&&b.email.toLowerCase()===emailKey));
   if(approve){
     // Jika diterima, alamat email dianggap selesai diproses dan stok dihapus.
     db.inventory=db.inventory.filter(item=>item.email.toLowerCase()!==emailKey);
   }else{
     // Jika ditolak, booking dilepas agar alamat bisa dibooking ulang.
     db.inventory.forEach(item=>{if(item.email.toLowerCase()===emailKey)item.bookedBy=null});
   }
 }
 if(approve&&u)u.balance+=2500;
 save();ownerView()
}
function reviewWithdrawal(id,approve){let x=db.withdrawals.find(x=>x.id===id&&x.status==="pending");if(!x)return;x.status=approve?"approved":"rejected";if(!approve){let u=db.users.find(u=>u.id===x.user);if(u)u.balance+=x.amount}save();ownerView()}
function toggleBan(id){let u=db.users.find(u=>u.id===id);if(u){u.banned=!u.banned;save();ownerView()}}
function exportData(){let b=new Blob([JSON.stringify(db,null,2)],{type:"application/json"}),a=document.createElement("a");a.href=URL.createObjectURL(b);a.download="luczz-gmail-backup.json";a.click();URL.revokeObjectURL(a.href)}
authScreen();
</script></body></html>
