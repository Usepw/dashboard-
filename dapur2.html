<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0">
<title>Kitchen Manager Dashboard</title>
<style>
  *{margin:0;padding:0;box-sizing:border-box;-webkit-tap-highlight-color:transparent;}
  :root{
    --primary:#0F172A;--accent:#2563EB;--bg:#F7F8FA;--card:#FFFFFF;
    --text:#0F172A;--text-soft:#475569;--text-mute:#94A3B8;
    --border:#E2E8F0;--danger:#DC2626;--success:#16A34A;--warning:#F59E0B;
    --radius:16px;--radius-sm:10px;
    --shadow:0 1px 3px rgba(15,23,42,.06),0 4px 12px rgba(15,23,42,.04);
  }
  body{font-family:-apple-system,BlinkMacSystemFont,'Segoe UI',Roboto,sans-serif;background:var(--bg);color:var(--text);font-size:15px;line-height:1.5;display:flex;justify-content:center;}
  #app{width:100%;max-width:520px;min-height:100vh;background:var(--bg);padding-bottom:24px;overflow-x:hidden;}
  
  .topbar{position:sticky;top:0;z-index:50;background:var(--card);border-bottom:1px solid var(--border);padding:14px 16px;display:flex;align-items:center;justify-content:space-between;}
  .topbar-title{font-weight:800;font-size:16px;}
  .topbar-title small{display:block;font-size:11px;color:var(--text-mute);font-weight:600;margin-top:2px;}
  
  .screen{padding:16px;animation:fade .22s ease;}
  @keyframes fade{from{opacity:0;transform:translateY(6px);}to{opacity:1;transform:none;}}

  .hero{background:linear-gradient(135deg,#1E293B 0%,#0F172A 100%);border-radius:20px;padding:20px 18px;color:#fff;margin-bottom:20px;box-shadow:0 8px 24px rgba(15,23,42,.15);}
  .hero-label{font-size:11px;letter-spacing:1px;text-transform:uppercase;opacity:.8;font-weight:700;}
  .hero-title{font-size:20px;font-weight:800;margin:5px 0 3px;}
  .hero-date{margin-top:12px;background:rgba(255,255,255,.1);padding:8px 12px;border-radius:8px;display:inline-block;font-size:13px;font-weight:600;}

  .section-title{font-weight:800;font-size:13.5px;color:var(--text-soft);margin:24px 0 12px;text-transform:uppercase;letter-spacing:.5px;display:flex;justify-content:space-between;}
  
  .card{background:var(--card);border-radius:var(--radius);padding:16px;box-shadow:var(--shadow);margin-bottom:12px;border:1px solid var(--border);}
  .card.alert{border-left:4px solid var(--danger);background:#FEF2F2;}
  .card.success{border-left:4px solid var(--success);background:#F0FDF4;}
  
  .menu-title{font-weight:800;font-size:14px;margin-bottom:4px;color:var(--text);}
  .menu-meta{font-size:12px;color:var(--text-soft);margin-bottom:10px;display:flex;gap:10px;}
  .menu-status{display:inline-flex;align-items:center;gap:5px;padding:4px 10px;border-radius:99px;font-size:10px;font-weight:800;}
  .status-fail{background:#FEE2E2;color:#991B1B;}
  .status-pass{background:#DCFCE7;color:#166534;}
  
  .check-grid{display:grid;grid-template-columns:1fr 1fr;gap:6px;margin-top:10px;}
  .check-item{font-size:11.5px;font-weight:600;display:flex;align-items:center;gap:5px;}

  /* KANBAN BOARD */
  .kanban-board{display:flex;gap:12px;overflow-x:auto;padding-bottom:16px;scroll-snap-type:x mandatory;-webkit-overflow-scrolling:touch;}
  .kanban-board::-webkit-scrollbar{display:none;}
  .kanban-col{flex:0 0 260px;scroll-snap-align:start;background:#F1F5F9;border-radius:12px;padding:12px;}
  .kanban-col-header{font-weight:800;font-size:12px;margin-bottom:12px;display:flex;justify-content:space-between;color:var(--text-soft);text-transform:uppercase;letter-spacing:.5px;}
  
  .kanban-card{background:var(--card);border-radius:10px;padding:12px;margin-bottom:10px;box-shadow:0 1px 2px rgba(0,0,0,.05);border:1px solid var(--border);}
  .kanban-card .title{font-weight:700;font-size:13px;line-height:1.3;margin-bottom:6px;}
  .kanban-card .meta{font-size:11px;color:var(--text-soft);display:flex;align-items:center;gap:6px;margin-bottom:8px;}
  .kanban-card .desc{font-size:11.5px;color:var(--text-soft);background:#F8FAFC;padding:8px;border-radius:6px;margin-bottom:8px;}
  .kanban-card .action{font-size:11px;color:var(--success);font-weight:600;margin-bottom:8px;}
  .kanban-tag{display:inline-block;font-size:9px;font-weight:800;padding:3px 6px;border-radius:4px;background:#E2E8F0;color:#475569;}

  .empty{padding:20px;text-align:center;color:var(--text-mute);font-size:13px;background:rgba(255,255,255,.5);border-radius:8px;}
  .loading{padding:40px;text-align:center;font-weight:700;color:var(--accent);}
  .error-box{background:#FEE2E2;color:#991B1B;padding:16px;border-radius:12px;font-size:13px;margin-bottom:16px;}
</style>
</head>
<body>
<div id="app">
  <div class="topbar">
    <div class="topbar-title">📊 Manager Dashboard<small>Sudimara Barat 2</small></div>
    <button onclick="fetchData()" style="background:var(--accent);color:#fff;border:none;padding:8px 12px;border-radius:8px;font-weight:700;font-size:12px;cursor:pointer;">↻ Refresh</button>
  </div>

  <div class="screen" id="main-screen">
    <div class="hero">
      <div class="hero-label">Kitchen Command Center</div>
      <div class="hero-title">Pantauan Harian</div>
      <div class="hero-date" id="todayDate">Memuat...</div>
    </div>

    <div id="loading" class="loading">⏳ Menghubungkan ke Google Sheets...</div>
    <div id="error" class="error-box" style="display:none;"></div>

    <div id="content" style="display:none;">
      
      <!-- VALIDASI HARIAN -->
      <div class="section-title">🍲 Validasi Menu Hari Ini</div>
      <div id="validasiContainer"></div>

      <!-- KANBAN PDCA -->
      <div class="section-title">📋 Papan Kanban (Tindak Lanjut)</div>
      <div class="kanban-board" id="kanbanContainer"></div>

    </div>
  </div>
</div>

<script>
// === GANTI URL INI DENGAN URL APPS SCRIPT ANDA ===
const API_URL = "https://script.google.com/macros/s/AKfycbxOq_a-8hXGcCiXKyA8gjBKuZhg5Lp7OJmKdKLLe476dSnsok3haP7fpTSGArgmivQ4wA/exec";

const today = new Date();
const todayStr = today.getFullYear() + '-' + String(today.getMonth()+1).padStart(2,'0') + '-' + String(today.getDate()).padStart(2,'0');
document.getElementById('todayDate').textContent = today.toLocaleDateString('id-ID', { weekday: 'long', year: 'numeric', month: 'long', day: 'numeric' });

async function fetchData() {
  document.getElementById('loading').style.display = 'block';
  document.getElementById('content').style.display = 'none';
  document.getElementById('error').style.display = 'none';

  if(API_URL === "URL_APPS_SCRIPT_ANDA_DI_SINI") {
    showError("Anda belum memasukkan URL Apps Script.");
    return;
  }

  try {
    const response = await fetch(`${API_URL}?action=getDashboardData&date=${todayStr}`);
    const data = await response.json();

    if (!data.success) throw new Error(data.error || "Gagal mengambil data");

    renderValidasi(data.validasi);
    renderKanban(data.kejadian, data.anggota);

    document.getElementById('loading').style.display = 'none';
    document.getElementById('content').style.display = 'block';

  } catch (err) {
    showError("Gagal terhubung ke database: " + err.message);
  }
}

function showError(msg) {
  document.getElementById('loading').style.display = 'none';
  const err = document.getElementById('error');
  err.textContent = "⚠️ " + msg;
  err.style.display = 'block';
}

function renderValidasi(rows) {
  const container = document.getElementById('validasiContainer');
  if (!rows || rows.length === 0) {
    container.innerHTML = `<div class="card empty">Belum ada validasi menu untuk hari ini.</div>`;
    return;
  }

  let html = '';
  rows.forEach(r => {
    const isPass = r['Status Keseluruhan'] === 'Sesuai' || r['Status Keseluruhan'] === 'Lulus';
    const cardClass = isPass ? 'success' : 'alert';
    const cek = (val) => val === 'Ya' ? '✅' : '❌';
    
    html += `
      <div class="card ${cardClass}">
        <div style="display:flex;justify-content:space-between;align-items:flex-start;">
          <div>
            <div class="menu-title">${r['Nama Menu'] || '-'}</div>
            <div class="menu-meta">
              <span>🍱 ${r['Komponen Menu'] || '-'}</span>
              <span>👨‍🍳 ${r['Koki Penanggung Jawab'] || '-'}</span>
            </div>
          </div>
          <div class="menu-status ${isPass ? 'status-pass' : 'status-fail'}">
            ${isPass ? 'LULUS' : 'PERIKSA'}
          </div>
        </div>
        
        <div class="check-grid">
          <div class="check-item">${cek(r['Rasa Sesuai Standar?'])} Rasa</div>
          <div class="check-item">${cek(r['Tekstur Sesuai Standar?'])} Tekstur</div>
          <div class="check-item">${cek(r['Visual Sesuai Standar?'])} Visual</div>
          <div class="check-item">${cek(r['Aroma Sesuai Standar?'])} Aroma</div>
        </div>
      </div>
    `;
  });
  container.innerHTML = html;
}

function renderKanban(kejadianRows, anggotaRows) {
  const container = document.getElementById('kanbanContainer');
  if (!kejadianRows || kejadianRows.length === 0) {
    container.innerHTML = `<div class="card empty" style="width:100%;">Belum ada data tindak lanjut.</div>`;
    return;
  }

  const columns = ['Backlog', 'In Progress', 'Verification', 'Done'];
  let html = '';

  columns.forEach(col => {
    // Filter data berdasarkan kolom Kanban
    const items = kejadianRows.filter(r => (r.kanban_status || '').trim().toLowerCase() === col.toLowerCase());
    
    html += `
      <div class="kanban-col">
        <div class="kanban-col-header">
          <span>${col}</span>
          <span style="background:#E2E8F0; padding:2px 6px; border-radius:4px; font-size:10px;">${items.length}</span>
        </div>
    `;

    if (items.length === 0) {
      html += `<div class="empty" style="font-size:11px; padding:12px;">Kosong</div>`;
    } else {
      items.forEach(r => {
        // Cari nama anggota
        let nama = r.member_id || 'Sistem';
        if(anggotaRows) {
          const member = anggotaRows.find(a => a.member_id === r.member_id);
          if(member) nama = member.nama;
        }
        
        let icon = '📝';
        if(r.kategori === 'Diskusi_1on1') icon = '🗣️';
        if(r.kategori === 'Pelanggaran') icon = '🔴';

        html += `
          <div class="kanban-card">
            <div class="title">${icon} ${r.judul || '-'}</div>
            <div class="meta">👤 ${nama}</div>
            
            ${r.deskripsi ? `<div class="desc">${r.deskripsi}</div>` : ''}
            ${r.tindakan ? `<div class="action">✅ ${r.tindakan}</div>` : ''}
            
            <div style="display:flex; justify-content:space-between; align-items:center; margin-top:8px;">
               <span class="kanban-tag">${r.pdca_phase || '-'}</span>
               ${r.follow_up_tanggal ? `<span style="font-size:10px; color:var(--danger); font-weight:700;">⏰ ${formatTgl(r.follow_up_tanggal)}</span>` : ''}
            </div>
          </div>
        `;
      });
    }

    html += `</div>`;
  });

  container.innerHTML = html;
}

function formatTgl(dateStr) {
  if (!dateStr) return '-';
  const d = new Date(dateStr);
  if (isNaN(d.getTime())) return dateStr;
  return d.toLocaleDateString('id-ID', { day: 'numeric', month: 'short' });
}

fetchData();
</script>
</body>
</html>
