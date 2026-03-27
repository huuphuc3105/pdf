<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Logo Placement Tool</title>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.7.1/jquery.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.11.174/pdf.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/pdf-lib/1.17.1/pdf-lib.min.js"></script>
<style>
@import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;600&family=Inter:wght@300;400;500;600&display=swap');
*{box-sizing:border-box;margin:0;padding:0}
html,body{height:100%;overflow:hidden;
  /* Illustrator-like light theme */
  background:#b0b0b0;
  color:#1a1a1a;
  font-family:'Inter',sans-serif;font-size:12px}

/* ── HEADER ── Illustrator top bar style ─ */
#hdr{
  height:40px;
  background:#535353;
  border-bottom:1px solid #3a3a3a;
  display:flex;align-items:center;padding:0 10px;gap:8px;flex-shrink:0;z-index:50;
  color:#e0e0e0;
}
.hbadge{
  background:#ff7c00;color:#fff;
  font-family:'JetBrains Mono',monospace;font-size:9px;font-weight:700;
  padding:2px 7px;letter-spacing:.06em;border-radius:2px;white-space:nowrap
}
.htitle{font-size:12px;font-weight:500;color:#e0e0e0;white-space:nowrap}
.hx{width:1px;height:16px;background:#666;flex-shrink:0}
.hi{font-family:'JetBrains Mono',monospace;font-size:10px;color:#aaa;white-space:nowrap;overflow:hidden;text-overflow:ellipsis;max-width:280px}
.hright{margin-left:auto;display:flex;align-items:center;gap:8px;flex-shrink:0}
.chk{display:flex;align-items:center;gap:4px;font-size:11px;color:#ccc;cursor:pointer;user-select:none;white-space:nowrap}
.chk input[type=checkbox]{accent-color:#ff7c00;width:12px;height:12px}

/* Tool button in header */
.htool{
  display:flex;align-items:center;gap:4px;
  padding:3px 8px;border-radius:3px;cursor:pointer;
  font-size:11px;color:#ddd;border:1px solid transparent;
  transition:all .15s;user-select:none;white-space:nowrap;
}
.htool:hover{background:rgba(255,255,255,.12);border-color:#888}
.htool.active{background:#ff7c00;color:#fff;border-color:#e06000}

/* GS badge */
.gs-badge{display:flex;align-items:center;gap:4px;font-family:'JetBrains Mono',monospace;font-size:9px;padding:2px 7px;border-radius:2px;cursor:pointer;transition:all .2s;white-space:nowrap}
.gs-ok  {background:rgba(34,197,94,.2);color:#16a34a;border:1px solid rgba(34,197,94,.4)}
.gs-err {background:rgba(239,68,68,.2);color:#dc2626;border:1px solid rgba(239,68,68,.4)}
.gs-unk {background:rgba(0,0,0,.15);color:#999;border:1px solid #777}

/* ── LAYOUT ── */
#app{display:flex;flex:1;height:calc(100vh - 40px);overflow:hidden}

/* ── SIDEBAR ── Illustrator panel style ─ */
#bar{
  width:240px;min-width:240px;
  background:#e8e8e8;
  border-right:1px solid #b8b8b8;
  overflow-y:auto;overflow-x:hidden;
  display:flex;flex-direction:column;
}
.sec{border-bottom:1px solid #cacaca;padding:10px 12px;flex-shrink:0}
.slbl{
  font-size:10px;font-weight:600;letter-spacing:.08em;text-transform:uppercase;
  color:#555;margin-bottom:8px;display:flex;align-items:center;gap:6px;
}
.slbl::after{content:'';flex:1;height:1px;background:#c0c0c0}

/* GS Panel */
#gsPanel{background:#fff8ee;border:1px solid #f0c080;border-radius:3px;padding:10px;margin-bottom:8px}
.gsp-ttl{color:#c06000;font-size:10px;font-weight:600;margin-bottom:6px}
.gsp-body{font-size:10px;color:#806030;line-height:1.6;margin-bottom:7px}
.gsp-body a{color:#ff7c00;text-decoration:none}.gsp-body a:hover{text-decoration:underline}
.gsp-body code{font-family:'JetBrains Mono',monospace;font-size:9px;background:rgba(255,124,0,.1);padding:1px 4px;border-radius:2px}
.gsp-row{display:flex;gap:5px}
.gsp-row input{flex:1;min-width:0;background:#fff;border:1px solid #ddb060;border-radius:2px;color:#604020;font-family:'JetBrains Mono',monospace;font-size:9px;padding:4px 6px;outline:none}
.gsp-row input:focus{border-color:#ff7c00}
.gsp-row button{background:#ff7c00;border:none;color:#fff;font-size:10px;font-weight:600;padding:0 8px;border-radius:2px;cursor:pointer}
.gsp-row button:hover{background:#e06000}
.gsp-or{font-size:10px;color:#a08060;text-align:center;margin:6px 0}

/* Upload zones */
.uz{border:1.5px dashed #b8b8b8;border-radius:3px;padding:10px 8px;text-align:center;cursor:pointer;transition:all .15s;background:#f4f4f4}
.uz:hover,.uz.drag{border-color:#ff7c00;background:rgba(255,124,0,.05)}
.uz.done{border-color:#22c55e;border-style:solid;background:rgba(34,197,94,.04)}
.uz.busy{border-color:#ff7c00;animation:blink .6s infinite alternate}
@keyframes blink{to{opacity:.4}}
.uz-ico{font-size:18px;margin-bottom:4px;display:block}
.uz p{font-size:10px;color:#777;line-height:1.4}
.uz strong{color:#ff7c00;font-weight:600}
.uz-fn{font-family:'JetBrains Mono',monospace;font-size:9px;color:#16a34a;margin-top:3px;overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
input[type=file]{display:none}

/* progress */
.pgw{display:none;margin-top:6px}
.pgw.on{display:block}
.pgbar{height:2px;background:#d0d0d0;border-radius:2px;overflow:hidden}
.pgfill{height:100%;background:#ff7c00;width:0;transition:width .25s;border-radius:2px}
.pgtxt{font-family:'JetBrains Mono',monospace;font-size:9px;color:#888;margin-top:3px;text-align:center}

/* logo preview */
#lprev{display:none;margin-top:7px;background:#fff;border:1px solid #d0d0d0;border-radius:3px;padding:7px;text-align:center}
#lprev img{max-width:100%;max-height:70px;object-fit:contain}
#linfo{font-family:'JetBrains Mono',monospace;font-size:9px;color:#888;margin-top:3px}

/* number inputs — Illustrator style */
.ng{display:grid;grid-template-columns:1fr 1fr;gap:5px;margin-bottom:8px}
.nf label{display:block;font-size:9px;color:#666;margin-bottom:2px;font-weight:500}
.nf input{
  width:100%;background:#fff;border:1px solid #c0c0c0;border-radius:2px;
  color:#1a1a1a;font-family:'JetBrains Mono',monospace;font-size:11px;
  padding:4px 6px;outline:none;transition:border-color .15s;
}
.nf input:focus{border-color:#ff7c00;box-shadow:0 0 0 2px rgba(255,124,0,.15)}

/* sliders */
.sr{display:flex;align-items:center;gap:6px;margin-bottom:6px}
.sr label{font-size:10px;color:#555;white-space:nowrap;min-width:48px;font-weight:500}
.sv{font-family:'JetBrains Mono',monospace;font-size:10px;color:#ff7c00;min-width:36px;text-align:right}
input[type=range]{flex:1;-webkit-appearance:none;height:3px;background:#c8c8c8;border-radius:2px;outline:none}
input[type=range]::-webkit-slider-thumb{-webkit-appearance:none;width:12px;height:12px;background:#ff7c00;border-radius:50%;cursor:pointer;border:1.5px solid #fff;box-shadow:0 1px 3px rgba(0,0,0,.3)}

/* buttons — Illustrator style */
.btn{display:flex;align-items:center;justify-content:center;gap:4px;width:100%;padding:6px 10px;border:1px solid #b8b8b8;border-radius:2px;font-family:'Inter',sans-serif;font-size:11px;font-weight:500;cursor:pointer;transition:all .15s;margin-bottom:5px;background:#e0e0e0;color:#1a1a1a}
.btn:last-child{margin-bottom:0}
.btn:disabled{opacity:.4;cursor:not-allowed}
.btn:not(:disabled):hover{background:#d0d0d0;border-color:#999}
.b-orange{background:#ff7c00;color:#fff;border-color:#e06000}
.b-orange:not(:disabled):hover{background:#e06000}
.b-green{background:#22c55e;color:#fff;border-color:#16a34a}
.b-green:not(:disabled):hover{background:#16a34a}
.brow{display:flex;gap:5px}.brow .btn{margin-bottom:0}

/* JSON box */
#jbox{display:none;margin-top:6px;background:#fff;border:1px solid #d0d0d0;border-radius:2px;padding:7px;font-family:'JetBrains Mono',monospace;font-size:8px;color:#666;white-space:pre-wrap;word-break:break-all;max-height:120px;overflow-y:auto;line-height:1.5}
#jbox.on{display:block}

/* ── Multi-logo overlays ── */
.logo-ov{position:absolute;cursor:move;z-index:10;user-select:none;display:none}
.logo-ov.on{display:block}
.logo-ov img{width:100%;height:100%;object-fit:contain;display:block;pointer-events:none}
.logo-ov .lsbd{position:absolute;inset:0;border:1.5px solid #ff7c00;pointer-events:none;border-radius:1px}
.logo-ov.selected .lsbd{border-color:#ff7c00;box-shadow:0 0 0 2px rgba(255,124,0,.2)}
.logo-ov.unselected .lsbd{border-color:rgba(160,160,160,.5);border-style:dashed}
.logo-ov.unselected:hover .lsbd{border-color:#ff9a40;border-style:solid}
.rh{position:absolute;width:8px;height:8px;background:#ff7c00;border:1.5px solid #fff;border-radius:1px;z-index:11;box-shadow:0 1px 3px rgba(0,0,0,.3)}
.rh.rNW{top:-4px;left:-4px;cursor:nw-resize}
.rh.rNE{top:-4px;right:-4px;cursor:ne-resize}
.rh.rSW{bottom:-4px;left:-4px;cursor:sw-resize}
.rh.rSE{bottom:-4px;right:-4px;cursor:se-resize}
.rstem{position:absolute;top:-18px;left:50%;width:1px;height:18px;background:#ff7c00;transform:translateX(-50%);pointer-events:none}
.rRot{position:absolute;top:-26px;left:50%;transform:translateX(-50%);width:12px;height:12px;background:#ff7c00;border-radius:50%;border:1.5px solid #fff;cursor:grab;display:flex;align-items:center;justify-content:center;font-size:8px;color:#fff;z-index:11}
.dl{position:absolute;font-family:'JetBrains Mono',monospace;font-size:8px;color:#003080;background:rgba(220,235,255,.92);padding:1px 4px;border-radius:2px;pointer-events:none;white-space:nowrap;border:1px solid rgba(0,80,180,.2)}
.dPos{top:-14px;left:0}.dW{bottom:-13px;left:50%;transform:translateX(-50%)}.dH{right:-36px;top:50%;transform:translateY(-50%)}

/* ── Logo list in sidebar ── */
#logoList{display:flex;flex-direction:column;gap:4px;margin-bottom:6px;max-height:160px;overflow-y:auto}
.logo-item{display:flex;align-items:center;gap:6px;background:#fff;border:1px solid #d0d0d0;border-radius:3px;padding:5px 7px;cursor:pointer;transition:all .15s}
.logo-item:hover{border-color:#ff7c00;background:#fff8f0}
.logo-item.active{border-color:#ff7c00;background:#fff3e6;box-shadow:0 0 0 2px rgba(255,124,0,.12)}
.logo-item-thumb{width:28px;height:28px;object-fit:contain;border:1px solid #e0e0e0;border-radius:2px;background:#f8f8f8;flex-shrink:0}
.logo-item-info{flex:1;min-width:0}
.logo-item-name{font-size:10px;font-weight:600;color:#333;overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.logo-item-dim{font-family:'JetBrains Mono',monospace;font-size:9px;color:#888}
.logo-item-del{width:18px;height:18px;border-radius:50%;background:rgba(200,40,40,.1);border:1px solid rgba(200,40,40,.25);color:#cc2222;font-size:11px;font-weight:700;cursor:pointer;display:flex;align-items:center;justify-content:center;flex-shrink:0;transition:all .15s;line-height:1}
.logo-item-del:hover{background:#cc2222;color:#fff;border-color:#cc2222}
.logo-empty{font-size:10px;color:#aaa;text-align:center;padding:10px 0;font-style:italic}

/* ── MEASURE PANEL in sidebar ── */
#measurePanel{background:#f0f8ff;border:1px solid #90c0e0;border-radius:3px;padding:10px;margin-bottom:0}
.meas-row{display:flex;justify-content:space-between;align-items:center;margin-bottom:5px}
.meas-lbl{font-size:10px;color:#555;font-weight:500}
.meas-val{font-family:'JetBrains Mono',monospace;font-size:11px;color:#1e60a0;font-weight:600}
.meas-clear{font-size:9px;color:#888;cursor:pointer;text-decoration:underline}
.meas-clear:hover{color:#cc0000}
#measureHint{font-size:9px;color:#888;line-height:1.5;margin-top:5px;font-style:italic}

/* ── CANVAS AREA ── */
#ca{flex:1;display:flex;flex-direction:column;overflow:hidden;background:#888;position:relative}

/* rulers — Illustrator style (light gray) */
#rc{position:absolute;top:0;left:0;width:22px;height:22px;background:#d4d4d4;border-right:1px solid #b0b0b0;border-bottom:1px solid #b0b0b0;z-index:30}
#rx{position:absolute;top:0;left:22px;right:0;height:22px;background:#d4d4d4;border-bottom:1px solid #b0b0b0;overflow:hidden;z-index:30}
#ry{position:absolute;top:22px;left:0;width:22px;bottom:28px;background:#d4d4d4;border-right:1px solid #b0b0b0;overflow:hidden;z-index:30}
canvas.ru{display:block}

/* crosshair */
#chx,#chy{position:absolute;pointer-events:none;z-index:20;display:none}
#chx{top:22px;bottom:28px;width:1px;background:rgba(0,100,200,.5)}
#chy{left:22px;right:0;height:1px;background:rgba(0,100,200,.5)}
#ctip{
  position:absolute;top:26px;left:26px;
  font-family:'JetBrains Mono',monospace;font-size:10px;
  color:#003080;background:rgba(220,235,255,.95);
  border:1px solid rgba(0,80,180,.4);padding:2px 7px;border-radius:2px;
  pointer-events:none;z-index:40;display:none;white-space:nowrap;
}

/* viewport */
#vp{position:absolute;top:22px;left:22px;right:0;bottom:28px;overflow:auto}

/* canvas wrapper — white page on gray canvas */
#cw{position:relative;display:inline-block;margin:20px;
  box-shadow:0 3px 16px rgba(0,0,0,.4);background:#ffffff;cursor:crosshair}
#pdfCv{display:block}
#gridCv{position:absolute;inset:0;pointer-events:none;z-index:2}

/* measure overlay canvas */
#measCv{position:absolute;inset:0;pointer-events:none;z-index:15}

/* logo overlay */
#logo{position:absolute;display:none;cursor:move;z-index:10;user-select:none}
#logo.on{display:block}
#logo img{width:100%;height:100%;object-fit:contain;display:block;pointer-events:none}
#sbd{position:absolute;inset:0;border:1px solid #ff7c00;pointer-events:none}
.rh{position:absolute;width:8px;height:8px;background:#ff7c00;border:1.5px solid #fff;border-radius:1px;z-index:11;box-shadow:0 1px 3px rgba(0,0,0,.3)}
#rNW{top:-4px;left:-4px;cursor:nw-resize}#rNE{top:-4px;right:-4px;cursor:ne-resize}
#rSW{bottom:-4px;left:-4px;cursor:sw-resize}#rSE{bottom:-4px;right:-4px;cursor:se-resize}
.rstem{position:absolute;top:-18px;left:50%;width:1px;height:18px;background:#ff7c00;transform:translateX(-50%);pointer-events:none}
#rRot{position:absolute;top:-26px;left:50%;transform:translateX(-50%);width:12px;height:12px;background:#ff7c00;border-radius:50%;border:1.5px solid #fff;cursor:grab;display:flex;align-items:center;justify-content:center;font-size:8px;color:#fff;z-index:11}
.dl{position:absolute;font-family:'JetBrains Mono',monospace;font-size:8px;color:#003080;background:rgba(220,235,255,.9);padding:1px 4px;border-radius:2px;pointer-events:none;white-space:nowrap;border:1px solid rgba(0,80,180,.2)}
#dPos{top:-14px;left:0}#dW{bottom:-13px;left:50%;transform:translateX(-50%)}#dH{right:-36px;top:50%;transform:translateY(-50%)}

/* status bar — Illustrator bottom bar */
#stbar{
  position:absolute;bottom:0;left:22px;right:0;height:28px;
  background:#535353;border-top:1px solid #3a3a3a;
  display:flex;align-items:center;padding:0 12px;gap:16px;
  font-family:'JetBrains Mono',monospace;font-size:10px;color:#bbb;z-index:30;
}
#stbar b{color:#ff9a40;font-weight:400}
#stMeas{color:#60b8ff;font-weight:600}

/* toast */
#toast{position:fixed;bottom:36px;right:12px;
  background:#fff;border:1px solid #d0d0d0;border-left:3px solid #ff7c00;
  padding:9px 14px;font-size:11px;border-radius:3px;
  box-shadow:0 4px 16px rgba(0,0,0,.2);z-index:9999;
  opacity:0;transform:translateY(6px);transition:all .2s;
  pointer-events:none;max-width:340px;line-height:1.5;color:#1a1a1a}
#toast.on{opacity:1;transform:translateY(0)}
#toast.ok{border-left-color:#22c55e}
#toast.err{border-left-color:#ef4444}
#toast.warn{border-left-color:#f59e0b}

/* loader */
#ld{display:none;position:fixed;inset:0;background:rgba(80,80,80,.7);align-items:center;justify-content:center;flex-direction:column;gap:12px;z-index:9000}
#ld.on{display:flex}
.spin{width:28px;height:28px;border:2px solid #ccc;border-top-color:#ff7c00;border-radius:50%;animation:sp .55s linear infinite}
@keyframes sp{to{transform:rotate(360deg)}}
#ld p{font-size:12px;color:#fff;text-shadow:0 1px 3px rgba(0,0,0,.5)}

::-webkit-scrollbar{width:6px;height:6px}
::-webkit-scrollbar-track{background:#d0d0d0}
::-webkit-scrollbar-thumb{background:#aaa;border-radius:3px}
::-webkit-scrollbar-thumb:hover{background:#888}
</style>
</head>
<body>

<!-- HEADER -->
<div id="hdr">
  <div class="hbadge">LOGO TOOL</div>
  <div class="htitle">Đặt Logo vào Rập PDF</div>
  <div class="hx"></div>
  <div class="hi" id="hPdf">Chưa tải PDF</div>
  <div class="hright">
    <!-- Tool mode buttons -->
    <div class="htool active" id="toolSelect" onclick="setTool('select')" title="Di chuyển logo (V)">
      ↖ Chọn
    </div>
    <div class="htool" id="toolMeasure" onclick="setTool('measure')" title="Đo khoảng cách (M)">
      ⟷ Đo mm
    </div>
    <div class="hx"></div>
    <label class="chk"><input type="checkbox" id="ckGrid"> Lưới</label>
    <label class="chk"><input type="checkbox" id="ckSnap"> Snap 5pt</label>
    <div class="hx"></div>
    <div class="hi" id="hZoom">—</div>
    <div class="hx"></div>
    <div id="gsBadge" class="gs-badge gs-unk"
         onclick="document.getElementById('gsPanel').scrollIntoView({behavior:'smooth'})">
      <span id="gsIcon">⬡</span><span id="gsText">GS…</span>
    </div>
  </div>
</div>

<!-- APP -->
<div id="app">

  <!-- SIDEBAR -->
  <div id="bar">

    <!-- ① PDF -->
    <div class="sec">
      <div class="slbl">① Upload PDF (Rập)</div>
      <div class="uz" id="pdfZone">
        <span class="uz-ico">📄</span>
        <p>Kéo thả <strong>file PDF</strong><br>hoặc click để chọn</p>
        <div class="uz-fn" id="pdfFn" style="display:none"></div>
      </div>
      <input type="file" id="pdfFile" accept=".pdf">
    </div>

    <!-- ② Logo -->
    <div class="sec">
      <div class="slbl">② Upload Logo (nhiều logo)</div>
      <div id="gsPanel" style="display:none">
        <div class="gsp-ttl">⚠ Ghostscript chưa tìm thấy</div>
        <div class="gsp-body">
          Cần GS để chuyển <strong>EPS→PNG</strong>.<br>
          <a href="https://www.ghostscript.com/releases/gsdnld.html" target="_blank">🔗 Tải Ghostscript</a><br><br>
          Nhập đường dẫn <code>gswin64c.exe</code>:
        </div>
        <div class="gsp-row">
          <input type="text" id="gsPathInput" placeholder="C:\Program Files\gs\...\gswin64c.exe">
          <button onclick="applyGsPath()">✓</button>
        </div>
        <div class="gsp-or">hoặc dùng PNG/JPG</div>
      </div>
      <!-- Logo list -->
      <div id="logoList"><div class="logo-empty">Chưa có logo nào</div></div>
      <!-- Upload zone - multiple files -->
      <div class="uz" id="epsZone">
        <span class="uz-ico">🎨</span>
        <p>Kéo thả <strong>EPS / PNG / SVG / JPG</strong><br>
           <span style="font-size:9px;color:#aaa">Có thể upload nhiều file cùng lúc</span></p>
      </div>
      <input type="file" id="epsFile" accept=".eps,.ai,.png,.jpg,.jpeg,.svg" multiple>
      <div class="pgw" id="pgW">
        <div class="pgbar"><div class="pgfill" id="pgF"></div></div>
        <div class="pgtxt" id="pgT"></div>
      </div>
    </div>

        <!-- ③ Position & Size -->
    <div class="sec">
      <div class="slbl">③ Logo đang chọn: <span id="selLogoName" style="color:#ff7c00;font-style:normal;font-size:9px">—</span></div>
      <div class="ng">
        <div class="nf"><label>X (pts)</label><input type="number" id="nX" value="0" step="1"></div>
        <div class="nf"><label>Y (pts)</label><input type="number" id="nY" value="0" step="1"></div>
        <div class="nf"><label>W (pts)</label><input type="number" id="nW" value="100" step="1" min="1"></div>
        <div class="nf"><label>H (pts)</label><input type="number" id="nH" value="100" step="1" min="1"></div>
        <div class="nf"><label>X (mm)</label><input type="number" id="nXmm" value="0.00" step="0.1" style="color:#c04000"></div>
        <div class="nf"><label>Y (mm)</label><input type="number" id="nYmm" value="0.00" step="0.1" style="color:#c04000"></div>
        <div class="nf"><label>W (mm)</label><input type="number" id="nWmm" value="35.28" step="0.1" style="color:#c04000"></div>
        <div class="nf"><label>H (mm)</label><input type="number" id="nHmm" value="35.28" step="0.1" style="color:#c04000"></div>
      </div>
      <div class="sr">
        <label>Xoay</label>
        <input type="range" id="sRot" min="-180" max="180" value="0" step="1">
        <span class="sv" id="vRot">0°</span>
      </div>
      <div class="sr">
        <label>Opacity</label>
        <input type="range" id="sOpa" min="10" max="100" value="100" step="1">
        <span class="sv" id="vOpa">100%</span>
      </div>
      <div class="brow" style="margin-top:6px">
        <button class="btn" id="btnCtr" disabled>⊕ Căn giữa</button>
        <button class="btn" id="btnRst" disabled>↺ Reset</button>
      </div>
    </div>

    <!-- ⟷ MEASURE -->
    <div class="sec">
      <div class="slbl">⟷ Đo khoảng cách</div>
      <div id="measurePanel">
        <div class="meas-row">
          <span class="meas-lbl">Khoảng cách</span>
          <span class="meas-val" id="measDist">—</span>
        </div>
        <div class="meas-row">
          <span class="meas-lbl">ΔX</span>
          <span class="meas-val" id="measDX">—</span>
        </div>
        <div class="meas-row">
          <span class="meas-lbl">ΔY</span>
          <span class="meas-val" id="measDY">—</span>
        </div>
        <div class="meas-row">
          <span class="meas-lbl">Góc</span>
          <span class="meas-val" id="measAngle">—</span>
        </div>
        <div style="display:flex;justify-content:space-between;margin-top:4px">
          <span class="meas-clear" onclick="clearMeasure()">✕ Xóa phép đo</span>
          <span style="font-size:9px;color:#888">72pt = 25.4mm</span>
        </div>
        <div id="measureHint">Chọn tool <b>⟷ Đo mm</b> rồi<br>click điểm đầu → click điểm cuối</div>
      </div>
    </div>

    <!-- Zoom -->
    <div class="sec">
      <div class="slbl">Zoom canvas</div>
      <div class="sr">
        <label>Zoom</label>
        <input type="range" id="sZ" min="20" max="300" value="75" step="5">
        <span class="sv" id="vZ">75%</span>
      </div>
      <div class="brow">
        <button class="btn" id="btnFit" style="font-size:10px">⊡ Fit</button>
        <button class="btn" id="btnZ1"  style="font-size:10px">1:1</button>
        <button class="btn" id="btnZ2"  style="font-size:10px">2:1</button>
      </div>
    </div>

    <!-- ④ Save & Export -->
    <div class="sec">
      <div class="slbl">④ Lưu & Xuất</div>
      <button class="btn b-green" id="btnSave" disabled>💾 Lưu vị trí → Server</button>
      <button class="btn b-orange" id="btnExp" disabled>⬇ Xuất PDF có Logo</button>
      <button class="btn" id="btnLoad" style="font-size:10px">📂 Tải placement đã lưu</button>
      <div id="jbox"></div>
    </div>

  </div><!-- /sidebar -->

  <!-- CANVAS AREA -->
  <div id="ca">
    <div id="rc"></div>
    <div id="rx"><canvas class="ru" id="rxCv" height="22"></canvas></div>
    <div id="ry"><canvas class="ru" id="ryCv" width="22"></canvas></div>
    <div id="chx"></div><div id="chy"></div>
    <div id="ctip"></div>

    <div id="vp">
      <div id="cw">
        <canvas id="pdfCv"></canvas>
        <canvas id="gridCv"></canvas>
        <canvas id="measCv"></canvas><!-- measure overlay -->

        <!-- Dynamic logo overlays injected here by JS -->
      </div>
    </div>

    <div id="stbar">
      <span>PDF <b id="sPdf">—</b></span>
      <span>Logo <b id="sLogo">—</b></span>
      <span>Pos <b id="sPos">—</b></span>
      <span>Cursor <b id="sCur">—</b></span>
      <span id="stMeasWrap" style="display:none">Đo: <b id="stMeas">—</b></span>
    </div>
  </div>

</div><!-- /app -->

<div id="toast"></div>
<div id="ld"><div class="spin"></div><p id="ldMsg">Đang xử lý…</p></div>

<script>

'use strict';

// ═══════════════════════════════════════════════════════
// CONFIG
// ═══════════════════════════════════════════════════════
const API = 'http://192.168.1.251:7780';
pdfjsLib.GlobalWorkerOptions.workerSrc =
  'https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.11.174/pdf.worker.min.js';

const PT2MM = 25.4 / 72;
const MM2PT = 72  / 25.4;

// ═══════════════════════════════════════════════════════
// STATE
// ═══════════════════════════════════════════════════════
const G = {
  // PDF
  pdfDoc:  null,
  pdfBuf:  null,   // Uint8Array — NOT ArrayBuffer (avoids detach)
  pdfName: '',
  pdfW: 0, pdfH: 0,

  // Multi-logo list
  logos: [],        // [{id, name, url, buf, nw, nh, px, py, pw, ph, rot, opa}]
  selId: null,      // currently selected logo id

  // Interaction
  drag: false, resize: null, rotating: false,
  _dragLid: null,   // logo id being dragged/resized/rotated
  _dragSx:0,_dragSy:0,_dragSpx:0,_dragSpy:0,
  _resSx:0,_resSy:0,_resSpx:0,_resSpy:0,_resSpw:0,_resSph:0,_resDir:'',
  _rotSa:0,_rotSr:0,
  gsOk: false,

  // Tool
  tool: 'select',
  zoom: 0.75,

  // Measure
  meas: { p1:null, p2:null, preview:null },
};

let _logoIdSeq = 0;
const newId = () => 'L' + (++_logoIdSeq);

const p2c  = v => v * G.zoom * (96/72);
const c2p  = v => v / (G.zoom * (96/72));
const ri   = v => Math.round(v);
const pf   = id => parseFloat($('#'+id).val()) || 0;
const sn   = v => $('#ckSnap').is(':checked') ? Math.round(v/5)*5 : v;
const fmm  = v => (v * PT2MM).toFixed(2) + ' mm';

function selLogo()  { return G.logos.find(l => l.id === G.selId) || null; }
function logoById(id){ return G.logos.find(l => l.id === id) || null; }

// ═══════════════════════════════════════════════════════
// TOAST / LOADING / PROGRESS
// ═══════════════════════════════════════════════════════
let _tt;
function toast(msg, type='') {
  clearTimeout(_tt);
  $('#toast').attr('class','toast on '+type).html(msg);
  _tt = setTimeout(() => $('#toast').removeClass('on'), 4000);
}
function loading(on, msg='Đang xử lý…') {
  $('#ldMsg').text(msg); $('#ld').toggleClass('on', on);
}
function prog(pct, txt) {
  if (pct < 0) { $('#pgW').removeClass('on'); return; }
  $('#pgW').addClass('on');
  $('#pgF').css('width', pct+'%'); $('#pgT').text(txt);
  if (pct >= 100) setTimeout(() => $('#pgW').removeClass('on'), 1200);
}
function updBtns() {
  const hasLogo = G.logos.length > 0;
  const hasPdf  = !!G.pdfDoc;
  const ok = hasPdf && hasLogo;
  $('#btnCtr,#btnRst,#btnSave,#btnExp').prop('disabled', !ok);
}

// ═══════════════════════════════════════════════════════
// TOOL SWITCHING
// ═══════════════════════════════════════════════════════
function setTool(t) {
  G.tool = t;
  $('#toolSelect,#toolMeasure').removeClass('active');
  if (t==='select')  $('#toolSelect').addClass('active');
  if (t==='measure') $('#toolMeasure').addClass('active');
  if (t === 'measure') {
    G.meas = {p1:null,p2:null,preview:null};
    drawMeasure();
    $('#measureHint').text('Click điểm đầu trên canvas…');
  }
}

// ═══════════════════════════════════════════════════════
// GS STATUS
// ═══════════════════════════════════════════════════════
function gsStatus(ok, ver) {
  G.gsOk = ok;
  if (ok) {
    $('#gsBadge').attr('class','gs-badge gs-ok');
    $('#gsIcon').text('●'); $('#gsText').text('GS '+(ver||'OK'));
    $('#gsPanel').hide();
  } else {
    $('#gsBadge').attr('class','gs-badge gs-err');
    $('#gsIcon').text('●'); $('#gsText').text('GS chưa cài');
    $('#gsPanel').show();
  }
}
function gsUnknown(msg) {
  $('#gsBadge').attr('class','gs-badge gs-unk');
  $('#gsIcon').text('⬡'); $('#gsText').text(msg||'Offline');
}
async function checkGs() {
  try {
    const r = await fetch(`${API}/api/ping`,{signal:AbortSignal.timeout(5000)});
    if(!r.ok) throw new Error('HTTP '+r.status);
    const p = await r.json();
    gsStatus(p.gs_ok, p.gs_version);
    return p;
  } catch(e) { gsUnknown('Server offline'); return null; }
}
async function applyGsPath() {
  const path = $('#gsPathInput').val().trim();
  if (!path) { toast('Nhập đường dẫn gswin64c.exe','warn'); return; }
  loading(true,'Đang kiểm tra GS…');
  try {
    const r = await fetch(`${API}/api/set-gs-path`,{
      method:'POST', headers:{'Content-Type':'application/json'},
      body: JSON.stringify({path}),
    });
    const d = await r.json();
    if (!r.ok||!d.success) throw new Error(d.error||'Thất bại');
    gsStatus(true, d.gs_version);
    toast(`✓ GS ${d.gs_version}`,'ok');
  } catch(e) { toast('✗ '+e.message.split('\n')[0],'err'); }
  finally { loading(false); }
}

// ═══════════════════════════════════════════════════════
// PDF UPLOAD
// ═══════════════════════════════════════════════════════
setupDrop($('#pdfZone'),$('#pdfFile'),['pdf'],handlePdf);
function handlePdf(file) {
  G.pdfName = file.name; loading(true,'Đang tải PDF…');
  const fr = new FileReader();
  fr.onload = async e => {
    G.pdfBuf = new Uint8Array(e.target.result);
    try {
      const data = G.pdfBuf.slice(); // copy — pdf.js transfers ownership
      G.pdfDoc = await pdfjsLib.getDocument({data}).promise;
      const pg = await G.pdfDoc.getPage(1);
      const vp = pg.getViewport({scale:1});
      G.pdfW=vp.width; G.pdfH=vp.height;
      await renderPdf();
      $('#pdfZone').addClass('done');
      $('#pdfFn').text(file.name).show();
      $('#hPdf').text(`${file.name}  |  ${ri(G.pdfW)}×${ri(G.pdfH)} pt  |  ${(G.pdfW*PT2MM).toFixed(1)}×${(G.pdfH*PT2MM).toFixed(1)} mm`);
      $('#sPdf').text(`${ri(G.pdfW)}×${ri(G.pdfH)} pt`);
      updBtns(); toast('Đã tải PDF ✓','ok');
    } catch(e) { toast('Lỗi PDF: '+e.message,'err'); }
    finally { loading(false); }
  };
  fr.readAsArrayBuffer(file);
}

// ═══════════════════════════════════════════════════════
// RENDER PDF
// ═══════════════════════════════════════════════════════
async function renderPdf() {
  if (!G.pdfDoc) return;
  const pg = await G.pdfDoc.getPage(1);
  const sc = G.zoom*(96/72);
  const vp = pg.getViewport({scale:sc});
  const cv = document.getElementById('pdfCv');
  cv.width=vp.width; cv.height=vp.height;
  await pg.render({canvasContext:cv.getContext('2d'),viewport:vp}).promise;
  ['gridCv','measCv'].forEach(id=>{
    const c=document.getElementById(id);
    c.width=vp.width; c.height=vp.height;
    c.style.width=vp.width+'px'; c.style.height=vp.height+'px';
  });
  drawGrid(); drawRulers();
  // Re-render all logo overlays
  G.logos.forEach(l => updateOverlay(l.id));
  drawMeasure();
  const pct=ri(G.zoom*100)+'%';
  $('#hZoom').text(pct); $('#vZ').text(pct);
}

// ═══════════════════════════════════════════════════════
// LOGO UPLOAD — multiple files
// ═══════════════════════════════════════════════════════
// Override setupDrop to support multiple files
$('#epsZone').on('click', () => $('#epsFile').trigger('click'));
$('#epsFile').on('change', function() {
  [...this.files].forEach(f => handleLogoFile(f));
  this.value = ''; // reset so same file can be added again
});
$('#epsZone').on('dragover', e => { e.preventDefault(); $('#epsZone').addClass('drag'); });
$('#epsZone').on('dragleave drop', () => $('#epsZone').removeClass('drag'));
$('#epsZone').on('drop', e => {
  e.preventDefault(); $('#epsZone').removeClass('drag');
  [...e.originalEvent.dataTransfer.files].forEach(f => {
    const ext = f.name.split('.').pop().toLowerCase();
    if (['eps','ai','png','jpg','jpeg','svg'].includes(ext)) handleLogoFile(f);
    else toast(`.${ext} không hỗ trợ`,'err');
  });
});

async function handleLogoFile(file) {
  const ext = file.name.split('.').pop().toLowerCase();
  if (['eps','ai'].includes(ext)) await convertEps(file);
  else await loadImgFile(file);
}

async function convertEps(file) {
  $('#epsZone').addClass('busy');
  prog(10,'Kiểm tra server…');
  let ping;
  try {
    const r=await fetch(`${API}/api/ping`,{signal:AbortSignal.timeout(5000)});
    if(!r.ok) throw new Error('HTTP '+r.status);
    ping=await r.json();
  } catch(e) {
    prog(-1); $('#epsZone').removeClass('busy'); gsUnknown('Offline');
    toast(`⚠ <b>Không kết nối API server</b><br><small>${API}</small>`,'err');
    return;
  }
  gsStatus(ping.gs_ok,ping.gs_version);
  if(!ping.gs_ok){
    prog(-1); $('#epsZone').removeClass('busy');
    toast(`⚠ <b>GS chưa cài</b> — upload PNG/JPG thay vì EPS`,'err');
    return;
  }
  prog(35,`GS ${ping.gs_version} — Upload ${file.name} (${_fmtSz(file.size)})…`);
  const fd=new FormData();
  fd.append('file',file,file.name);
  try {
    prog(55,'Chuyển EPS → PNG…');
    const resp=await fetch(`${API}/api/convert-eps`,{method:'POST',body:fd});
    let result;
    try{result=await resp.json();}catch(e){throw new Error(`HTTP ${resp.status}`);}
    if(!resp.ok||!result.success) throw new Error(result.message||result.error||`HTTP ${resp.status}`);
    prog(90,'Hiển thị…');
    const url='data:image/png;base64,'+result.png_base64;
    addLogo(url,result.filename||file.name,result.width,result.height,b64u8(result.png_base64));
    prog(100,`✓ ${result.width}×${result.height}px`);
    toast(`${file.name} → PNG ✓`,'ok');
  } catch(e){
    prog(-1);
    toast(`✗ ${file.name}: ${(e.message||'').slice(0,150)}`,'err');
  } finally {$('#epsZone').removeClass('busy');}
}

async function loadImgFile(file) {
  const url=await fr2url(file);
  const img=new Image();
  img.onload=()=>{addLogo(url,file.name,img.naturalWidth,img.naturalHeight,url2u8(url));toast(`${file.name} đã tải ✓`,'ok');};
  img.onerror=()=>toast(`Không đọc được ${file.name}`,'err');
  img.src=url;
}

// ═══════════════════════════════════════════════════════
// ADD / REMOVE / SELECT LOGO
// ═══════════════════════════════════════════════════════
function addLogo(url, name, nw, nh, buf) {
  const id = newId();
  const logo = {
    id, name, url, buf, nw, nh,
    px: 20 + G.logos.length*15,  // stagger position
    py: 20 + G.logos.length*15,
    pw: 150,
    ph: ri(150*nh/nw),
    rot: 0, opa: 1.0,
  };
  G.logos.push(logo);
  createOverlayEl(id);
  updateOverlay(id);
  renderLogoList();
  selectLogo(id);
  updBtns();
  $('#sLogo').text(G.logos.length);
}

function removeLogo(id) {
  // Remove overlay element
  $(`#ov-${id}`).remove();
  G.logos = G.logos.filter(l=>l.id!==id);
  // Select another logo if needed
  if (G.selId===id) {
    G.selId = G.logos.length ? G.logos[G.logos.length-1].id : null;
  }
  renderLogoList();
  syncIn();
  updBtns();
  $('#sLogo').text(G.logos.length);
  if (!G.logos.length) {
    $('#selLogoName').text('—');
    ['nX','nY','nW','nH','nXmm','nYmm','nWmm','nHmm'].forEach(id=>$('#'+id).val(''));
    $('#sRot').val(0);$('#vRot').text('0°');
    $('#sOpa').val(100);$('#vOpa').text('100%');
  }
}

function selectLogo(id) {
  const prev = G.selId;
  G.selId = id;
  // Update overlay classes
  G.logos.forEach(l => {
    const el = document.getElementById(`ov-${l.id}`);
    if (!el) return;
    if (l.id===id) { el.className='logo-ov on selected'; }
    else           { el.className='logo-ov on unselected'; }
    // Show/hide handles
    el.querySelectorAll('.rh,.rstem,.rRot').forEach(h=>{
      h.style.display = l.id===id ? '' : 'none';
    });
  });
  renderLogoList();
  syncIn();
  const logo = logoById(id);
  if (logo) $('#selLogoName').text(logo.name);
}

// ═══════════════════════════════════════════════════════
// LOGO LIST in sidebar
// ═══════════════════════════════════════════════════════
function renderLogoList() {
  const $list = $('#logoList');
  $list.empty();
  if (!G.logos.length) {
    $list.html('<div class="logo-empty">Chưa có logo nào</div>');
    return;
  }
  G.logos.forEach(logo => {
    const isActive = logo.id === G.selId;
    const $item = $(`
      <div class="logo-item ${isActive?'active':''}" data-id="${logo.id}">
        <img class="logo-item-thumb" src="${logo.url}" alt="">
        <div class="logo-item-info">
          <div class="logo-item-name" title="${logo.name}">${logo.name}</div>
          <div class="logo-item-dim">${ri(logo.pw)}×${ri(logo.ph)} pt</div>
        </div>
        <div class="logo-item-del" title="Xóa logo này">✕</div>
      </div>
    `);
    $item.on('click', function(e) {
      if ($(e.target).hasClass('logo-item-del')) return;
      selectLogo(logo.id);
    });
    $item.find('.logo-item-del').on('click', e => {
      e.stopPropagation();
      removeLogo(logo.id);
    });
    $list.append($item);
  });
}

// ═══════════════════════════════════════════════════════
// CREATE / UPDATE OVERLAY ELEMENT
// ═══════════════════════════════════════════════════════
function createOverlayEl(id) {
  const el = document.createElement('div');
  el.id = `ov-${id}`;
  el.className = 'logo-ov';
  el.innerHTML = `
    <img src="" alt="" draggable="false">
    <div class="lsbd"></div>
    <div class="rh rNW"></div><div class="rh rNE"></div>
    <div class="rh rSW"></div><div class="rh rSE"></div>
    <div class="rstem"></div>
    <div class="rRot">↻</div>
    <div class="dl dPos"></div>
    <div class="dl dW"></div>
    <div class="dl dH"></div>
  `;
  document.getElementById('cw').appendChild(el);

  // Set logo image
  el.querySelector('img').src = logoById(id)?.url || '';

  // Bind drag
  $(el).on('mousedown', e => {
    if (G.tool !== 'select') return;
    if ($(e.target).hasClass('rh')||$(e.target).hasClass('rRot')) return;
    e.preventDefault(); e.stopPropagation();
    selectLogo(id);
    G.drag=true; G._dragLid=id;
    G._dragSx=e.clientX; G._dragSy=e.clientY;
    const l=logoById(id);
    G._dragSpx=l.px; G._dragSpy=l.py;
    el.style.cursor='grabbing';
  });

  // Bind resize handles
  el.querySelectorAll('.rh').forEach(rh => {
    $(rh).on('mousedown', e => {
      if (G.tool !== 'select') return;
      e.preventDefault(); e.stopPropagation();
      selectLogo(id);
      const dir = [...rh.classList].find(c=>['rNW','rNE','rSW','rSE'].includes(c))||'';
      G.resize=true; G._dragLid=id; G._resDir=dir.toLowerCase().slice(1);
      G._resSx=e.clientX; G._resSy=e.clientY;
      const l=logoById(id);
      G._resSpx=l.px; G._resSpy=l.py; G._resSpw=l.pw; G._resSph=l.ph;
    });
  });

  // Bind rotate handle
  const rotH = el.querySelector('.rRot');
  $(rotH).on('mousedown', e => {
    if (G.tool !== 'select') return;
    e.preventDefault(); e.stopPropagation();
    selectLogo(id);
    G.rotating=true; G._dragLid=id;
    const rc=el.getBoundingClientRect();
    G._rotSa=Math.atan2(e.clientY-rc.top-rc.height/2,e.clientX-rc.left-rc.width/2)*180/Math.PI;
    G._rotSr=logoById(id)?.rot||0;
  });
}

function updateOverlay(id) {
  const logo = logoById(id);
  if (!logo) return;
  const el = document.getElementById(`ov-${id}`);
  if (!el) return;
  const isSel = id===G.selId;
  el.className = `logo-ov on ${isSel?'selected':'unselected'}`;
  el.style.cssText = `left:${p2c(logo.px)}px;top:${p2c(logo.py)}px;width:${p2c(logo.pw)}px;height:${p2c(logo.ph)}px;transform:rotate(${logo.rot}deg);opacity:${logo.opa};`;
  el.querySelector('.dPos').textContent=`${ri(logo.px)},${ri(logo.py)} pt`;
  el.querySelector('.dW').textContent=fmm(logo.pw);
  el.querySelector('.dH').textContent=fmm(logo.ph);
  // Show/hide handles
  el.querySelectorAll('.rh,.rstem,.rRot').forEach(h=>{h.style.display=isSel?'':'none';});
}

// ═══════════════════════════════════════════════════════
// SYNC INPUTS ↔ SELECTED LOGO
// ═══════════════════════════════════════════════════════
function syncIn() {
  const l=selLogo();
  if(!l){return;}
  $('#nX').val(ri(l.px));   $('#nY').val(ri(l.py));
  $('#nW').val(ri(l.pw));   $('#nH').val(ri(l.ph));
  $('#nXmm').val((l.px*PT2MM).toFixed(2));
  $('#nYmm').val((l.py*PT2MM).toFixed(2));
  $('#nWmm').val((l.pw*PT2MM).toFixed(2));
  $('#nHmm').val((l.ph*PT2MM).toFixed(2));
  $('#sRot').val(l.rot);  $('#vRot').text(l.rot+'°');
  $('#sOpa').val(ri(l.opa*100)); $('#vOpa').text(ri(l.opa*100)+'%');
  $('#sPos').text(`x=${ri(l.px)} y=${ri(l.py)} w=${ri(l.pw)} h=${ri(l.ph)}`);
}

function fromInPt() {
  const l=selLogo(); if(!l) return;
  l.px=pf('nX'); l.py=pf('nY');
  l.pw=Math.max(1,pf('nW')); l.ph=Math.max(1,pf('nH'));
  $('#nXmm').val((l.px*PT2MM).toFixed(2));
  $('#nYmm').val((l.py*PT2MM).toFixed(2));
  $('#nWmm').val((l.pw*PT2MM).toFixed(2));
  $('#nHmm').val((l.ph*PT2MM).toFixed(2));
  updateOverlay(l.id);
}
function fromInMm() {
  const l=selLogo(); if(!l) return;
  l.px=pf('nXmm')*MM2PT; l.py=pf('nYmm')*MM2PT;
  l.pw=Math.max(1,pf('nWmm')*MM2PT); l.ph=Math.max(1,pf('nHmm')*MM2PT);
  $('#nX').val(ri(l.px));$('#nY').val(ri(l.py));
  $('#nW').val(ri(l.pw));$('#nH').val(ri(l.ph));
  updateOverlay(l.id);
}

$('#nX,#nY,#nW,#nH').on('input change', fromInPt);
$('#nXmm,#nYmm,#nWmm,#nHmm').on('input change', fromInMm);
$('#sRot').on('input', function(){const l=selLogo();if(!l)return;l.rot=+$(this).val();$('#vRot').text(l.rot+'°');updateOverlay(l.id);});
$('#sOpa').on('input', function(){const l=selLogo();if(!l)return;l.opa=+$(this).val()/100;$('#vOpa').text($(this).val()+'%');updateOverlay(l.id);});
$('#btnCtr').on('click',()=>{const l=selLogo();if(!l)return;l.px=(G.pdfW-l.pw)/2;l.py=(G.pdfH-l.ph)/2;syncIn();updateOverlay(l.id);});
$('#btnRst').on('click',()=>{const l=selLogo();if(!l)return;l.px=0;l.py=0;l.pw=150;l.ph=ri(150*l.nh/l.nw);l.rot=0;l.opa=1;syncIn();updateOverlay(l.id);});

// ═══════════════════════════════════════════════════════
// GLOBAL MOUSE EVENTS (drag / resize / rotate all logos)
// ═══════════════════════════════════════════════════════
$(document).on('mousemove', e => {
  if (G.drag && G._dragLid) {
    const l=logoById(G._dragLid); if(!l) return;
    l.px=sn(G._dragSpx+c2p(e.clientX-G._dragSx));
    l.py=sn(G._dragSpy+c2p(e.clientY-G._dragSy));
    updateOverlay(l.id); syncIn();
  }
  if (G.resize && G._dragLid) {
    const l=logoById(G._dragLid); if(!l) return;
    const dx=c2p(e.clientX-G._resSx), dy=c2p(e.clientY-G._resSy);
    const d=G._resDir;
    let nx=G._resSpx,ny=G._resSpy,nw=G._resSpw,nh=G._resSph;
    if(d.includes('e')) nw=Math.max(5,G._resSpw+dx);
    if(d.includes('w')){nx=G._resSpx+dx;nw=Math.max(5,G._resSpw-dx);}
    if(d.includes('s')) nh=Math.max(5,G._resSph+dy);
    if(d.includes('n')){ny=G._resSpy+dy;nh=Math.max(5,G._resSph-dy);}
    l.px=sn(nx);l.py=sn(ny);l.pw=sn(nw);l.ph=sn(nh);
    updateOverlay(l.id); syncIn();
  }
  if (G.rotating && G._dragLid) {
    const l=logoById(G._dragLid); if(!l) return;
    const el=document.getElementById(`ov-${l.id}`);
    if(!el) return;
    const rc=el.getBoundingClientRect();
    const a=Math.atan2(e.clientY-rc.top-rc.height/2,e.clientX-rc.left-rc.width/2)*180/Math.PI;
    l.rot=ri(G._rotSr+a-G._rotSa);
    $('#sRot').val(l.rot);$('#vRot').text(l.rot+'°');
    updateOverlay(l.id);
  }
  // Measure preview
  if (G.tool==='measure' && G.meas.p1 && !G.meas.p2) {
    G.meas.preview=cwPt(e); drawMeasure();
  }
});

$(document).on('mouseup', () => {
  if (G.drag) {
    G.drag=false;
    const el=document.getElementById(`ov-${G._dragLid}`);
    if(el) el.style.cursor='move';
    // Update list dim display
    renderLogoList();
  }
  G.drag=false; G.resize=false; G.rotating=false;
  G._dragLid=null;
});

// Click on canvas background → deselect
$('#cw').on('mousedown', e => {
  if (G.tool==='select' && e.target.id==='cw' || e.target.id==='pdfCv' || e.target.id==='gridCv') {
    G.selId=null;
    G.logos.forEach(l=>{
      const el=document.getElementById(`ov-${l.id}`);
      if(el){el.className='logo-ov on unselected';el.querySelectorAll('.rh,.rstem,.rRot').forEach(h=>h.style.display='none');}
    });
    renderLogoList();
    $('#selLogoName').text('—');
  }
});

// ═══════════════════════════════════════════════════════
// MEASURE TOOL
// ═══════════════════════════════════════════════════════
function cwPt(e) {
  const rc=document.getElementById('cw').getBoundingClientRect();
  return { x:c2p(e.clientX-rc.left), y:c2p(e.clientY-rc.top) };
}

$('#cw').on('click', function(e) {
  if (G.tool!=='measure' || !G.pdfDoc) return;
  const pt=cwPt(e);
  if (!G.meas.p1 || (G.meas.p1 && G.meas.p2)) {
    G.meas.p1=pt; G.meas.p2=null; G.meas.preview=null;
    $('#measureHint').text('Click điểm cuối để hoàn thành…');
    drawMeasure();
  } else {
    G.meas.p2=pt;
    updateMeasurePanel(); drawMeasure();
    $('#measureHint').text('Click điểm đầu để đo lại.');
  }
});

$('#cw').on('mousemove', function(e) {
  if (G.tool==='measure' && G.meas.p1 && !G.meas.p2) {
    G.meas.preview=cwPt(e); drawMeasure();
  }
});

function updateMeasurePanel() {
  if(!G.meas.p1||!G.meas.p2) return;
  const dx=G.meas.p2.x-G.meas.p1.x, dy=G.meas.p2.y-G.meas.p1.y;
  const dist=Math.sqrt(dx*dx+dy*dy);
  const angle=Math.atan2(dy,dx)*180/Math.PI;
  $('#measDist').text(`${(dist*PT2MM).toFixed(2)} mm  (${ri(dist)} pt)`);
  $('#measDX').text(`${(Math.abs(dx)*PT2MM).toFixed(2)} mm`);
  $('#measDY').text(`${(Math.abs(dy)*PT2MM).toFixed(2)} mm`);
  $('#measAngle').text(`${angle.toFixed(1)}°`);
  $('#stMeasWrap').show(); $('#stMeas').text(`${(dist*PT2MM).toFixed(2)} mm`);
}

function clearMeasure() {
  G.meas={p1:null,p2:null,preview:null};
  $('#measDist,#measDX,#measDY,#measAngle').text('—');
  $('#measureHint').text('Chọn tool ⟷ Đo mm rồi\nclick điểm đầu → click điểm cuối');
  $('#stMeasWrap').hide(); drawMeasure();
}

function drawMeasure() {
  const cv=document.getElementById('measCv');
  if(!cv||!cv.width) return;
  const ctx=cv.getContext('2d');
  ctx.clearRect(0,0,cv.width,cv.height);
  const p1=G.meas.p1, p2=G.meas.p2||G.meas.preview;
  if(!p1) return;
  const x1=p2c(p1.x),y1=p2c(p1.y);
  _drawMeasPt(ctx,x1,y1,'#1e60a0');
  if(!p2) return;
  const x2=p2c(p2.x),y2=p2c(p2.y);
  const dx=p2.x-p1.x,dy=p2.y-p1.y;
  const dist=Math.sqrt(dx*dx+dy*dy);
  const distMm=(dist*PT2MM).toFixed(2);
  const angle=Math.atan2(y2-y1,x2-x1);
  const perp=angle+Math.PI/2;
  // dashed line
  ctx.save(); ctx.setLineDash([4,3]);
  ctx.strokeStyle=G.meas.p2?'#1e60a0':'#5090c0'; ctx.lineWidth=1.5;
  ctx.beginPath();ctx.moveTo(x1,y1);ctx.lineTo(x2,y2);ctx.stroke();
  ctx.restore();
  // end ticks
  [[x1,y1],[x2,y2]].forEach(([px,py])=>{
    ctx.save();ctx.strokeStyle='#1e60a0';ctx.lineWidth=2;
    ctx.beginPath();ctx.moveTo(px+Math.cos(perp)*8,py+Math.sin(perp)*8);ctx.lineTo(px-Math.cos(perp)*8,py-Math.sin(perp)*8);ctx.stroke();ctx.restore();
  });
  _drawArrow(ctx,x1,y1,x2,y2,'#1e60a0');
  _drawArrow(ctx,x2,y2,x1,y1,'#1e60a0');
  // distance label
  const mx=(x1+x2)/2,my=(y1+y2)/2;
  ctx.save();ctx.font='bold 11px "JetBrains Mono",monospace';
  const tw=ctx.measureText(distMm+' mm').width;
  ctx.fillStyle='rgba(30,96,160,.92)';
  ctx.beginPath();ctx.roundRect(mx-tw/2-5,my-14,tw+10,18,3);ctx.fill();
  ctx.fillStyle='#fff';ctx.textAlign='center';ctx.textBaseline='middle';
  ctx.fillText(distMm+' mm',mx,my);ctx.restore();
  // delta lines
  if(G.meas.p2&&(Math.abs(dx)>5||Math.abs(dy)>5)){
    ctx.save();ctx.setLineDash([2,4]);ctx.strokeStyle='rgba(80,140,220,.5)';ctx.lineWidth=1;
    ctx.beginPath();ctx.moveTo(x1,y1);ctx.lineTo(x2,y1);ctx.stroke();
    ctx.beginPath();ctx.moveTo(x2,y1);ctx.lineTo(x2,y2);ctx.stroke();
    ctx.restore();
    if(Math.abs(dx)>20) _measLbl(ctx,(x1+x2)/2,y1-13,`ΔX ${(Math.abs(dx)*PT2MM).toFixed(1)}mm`);
    if(Math.abs(dy)>20) _measLbl(ctx,x2+4,(y1+y2)/2,`ΔY ${(Math.abs(dy)*PT2MM).toFixed(1)}mm`,true);
  }
  _drawMeasPt(ctx,x2,y2,G.meas.p2?'#1e60a0':'#5090c0');
}
function _drawMeasPt(ctx,x,y,c){ctx.save();ctx.strokeStyle=c;ctx.lineWidth=1.5;ctx.fillStyle='#fff';ctx.beginPath();ctx.moveTo(x-8,y);ctx.lineTo(x+8,y);ctx.stroke();ctx.beginPath();ctx.moveTo(x,y-8);ctx.lineTo(x,y+8);ctx.stroke();ctx.beginPath();ctx.arc(x,y,4,0,Math.PI*2);ctx.fill();ctx.stroke();ctx.restore();}
function _drawArrow(ctx,x1,y1,x2,y2,c){const a=Math.atan2(y2-y1,x2-x1),s=6;ctx.save();ctx.fillStyle=c;ctx.beginPath();ctx.moveTo(x1,y1);ctx.lineTo(x1+Math.cos(a+2.5)*s,y1+Math.sin(a+2.5)*s);ctx.lineTo(x1+Math.cos(a-2.5)*s,y1+Math.sin(a-2.5)*s);ctx.closePath();ctx.fill();ctx.restore();}
function _measLbl(ctx,x,y,text,vertical=false){ctx.save();ctx.font='9px "JetBrains Mono",monospace';if(vertical){ctx.translate(x,y);ctx.rotate(-Math.PI/2);x=0;y=0;}const tw=ctx.measureText(text).width;ctx.fillStyle='rgba(80,140,200,.85)';ctx.beginPath();ctx.roundRect(x-tw/2-3,y-7,tw+6,14,2);ctx.fill();ctx.fillStyle='#fff';ctx.textAlign='center';ctx.textBaseline='middle';ctx.fillText(text,x,y);ctx.restore();}

// ═══════════════════════════════════════════════════════
// CROSSHAIR + COORD
// ═══════════════════════════════════════════════════════
$('#cw').on('mousemove', function(e) {
  const rc=this.getBoundingClientRect(), vp=document.getElementById('vp');
  const px=e.clientX-rc.left, py=e.clientY-rc.top;
  const cx=px+22-vp.scrollLeft, cy=py+22-vp.scrollTop;
  $('#chx').css({display:'block',left:cx+'px'});
  $('#chy').css({display:'block',top:cy+'px'});
  const ptX=c2p(px), ptY=c2p(py);
  $('#ctip').css({display:'block',left:(cx+8)+'px',top:(cy+3)+'px'})
    .text(`${(ptX*PT2MM).toFixed(2)}, ${(ptY*PT2MM).toFixed(2)} mm  (${ri(ptX)}, ${ri(ptY)} pt)`);
  $('#sCur').text(`${(ptX*PT2MM).toFixed(1)}, ${(ptY*PT2MM).toFixed(1)} mm`);
}).on('mouseleave', ()=>$('#chx,#chy,#ctip').hide());

$('#vp').on('scroll', drawRulers);

// ═══════════════════════════════════════════════════════
// RULERS (mm)
// ═══════════════════════════════════════════════════════
function drawRulers(){drawRX();drawRY();}
function drawRX(){
  const W=$('#rx')[0].offsetWidth, cv=document.getElementById('rxCv');
  cv.width=W; const ctx=cv.getContext('2d');
  ctx.fillStyle='#d4d4d4';ctx.fillRect(0,0,W,22);
  const cs=G.zoom*(96/72), off=20-$('#vp')[0].scrollLeft;
  const step_mm=pickMmStep(PT2MM/cs), step_pt=step_mm*MM2PT;
  ctx.strokeStyle='#888';ctx.fillStyle='#444';ctx.font='8px "JetBrains Mono",monospace';ctx.lineWidth=1;
  for(let pt=Math.floor(-off/cs/step_pt)*step_pt;pt<=(W-off)/cs;pt+=step_pt){
    const x=Math.round(off+pt*cs)+.5;if(x<0||x>W)continue;
    const mm=pt*PT2MM,mj=Math.abs(mm%(step_mm*5))<0.01;
    ctx.beginPath();ctx.moveTo(x,mj?5:12);ctx.lineTo(x,22);ctx.stroke();
    if(mj&&x>5)ctx.fillText(ri(mm),x+2,9);
  }
  ctx.fillStyle='#666';ctx.font='7px sans-serif';ctx.fillText('mm',2,9);
}
function drawRY(){
  const H=$('#ry')[0].offsetHeight, cv=document.getElementById('ryCv');
  cv.height=H; const ctx=cv.getContext('2d');
  ctx.fillStyle='#d4d4d4';ctx.fillRect(0,0,22,H);
  const cs=G.zoom*(96/72), off=20-$('#vp')[0].scrollTop;
  const step_mm=pickMmStep(PT2MM/cs), step_pt=step_mm*MM2PT;
  ctx.strokeStyle='#888';ctx.fillStyle='#444';ctx.font='8px "JetBrains Mono",monospace';ctx.lineWidth=1;
  for(let pt=Math.floor(-off/cs/step_pt)*step_pt;pt<=(H-off)/cs;pt+=step_pt){
    const y=Math.round(off+pt*cs)+.5;if(y<0||y>H)continue;
    const mm=pt*PT2MM,mj=Math.abs(mm%(step_mm*5))<0.01;
    ctx.beginPath();ctx.moveTo(22,y);ctx.lineTo(mj?5:12,y);ctx.stroke();
    if(mj&&y>12){ctx.save();ctx.translate(10,y-2);ctx.rotate(-Math.PI/2);ctx.fillText(ri(mm),0,0);ctx.restore();}
  }
}
function pickMmStep(mmPerPx){for(const s of[0.5,1,2,5,10,20,50,100])if(s/mmPerPx>=18)return s;return 100;}

// ═══════════════════════════════════════════════════════
// GRID
// ═══════════════════════════════════════════════════════
function drawGrid(){
  const cv=document.getElementById('gridCv');
  const W=document.getElementById('pdfCv').width||0;
  const H=document.getElementById('pdfCv').height||0;
  cv.width=W;cv.height=H;cv.style.width=W+'px';cv.style.height=H+'px';
  const ctx=cv.getContext('2d');ctx.clearRect(0,0,W,H);
  if(!$('#ckGrid').is(':checked'))return;
  const cs=G.zoom*(96/72);
  const step=(pickMmStep(PT2MM/cs)*5)*MM2PT*cs;
  ctx.strokeStyle='rgba(0,80,200,.07)';ctx.lineWidth=.5;
  for(let x=0;x<W;x+=step){ctx.beginPath();ctx.moveTo(x,0);ctx.lineTo(x,H);ctx.stroke();}
  for(let y=0;y<H;y+=step){ctx.beginPath();ctx.moveTo(0,y);ctx.lineTo(W,y);ctx.stroke();}
}
$('#ckGrid').on('change',drawGrid);

// ═══════════════════════════════════════════════════════
// ZOOM
// ═══════════════════════════════════════════════════════
$('#sZ').on('input', async function(){
  G.zoom=+$(this).val()/100;$('#vZ').text($(this).val()+'%');
  if(G.pdfDoc){loading(true,'Rendering…');await renderPdf();loading(false);}
});
$('#btnFit').on('click', async()=>{
  if(!G.pdfDoc)return;
  const vp=document.getElementById('vp');
  G.zoom=Math.max(.2,Math.min(3,Math.min((vp.offsetWidth-40)/G.pdfW,(vp.offsetHeight-40)/G.pdfH)/(96/72)));
  $('#sZ').val(ri(G.zoom*100));
  loading(true,'Rendering…');await renderPdf();loading(false);
});
$('#btnZ1').on('click',async()=>{G.zoom=72/96;$('#sZ').val(ri(G.zoom*100));if(G.pdfDoc){loading(true,'Rendering…');await renderPdf();loading(false);}});
$('#btnZ2').on('click',async()=>{G.zoom=144/96;$('#sZ').val(ri(G.zoom*100));if(G.pdfDoc){loading(true,'Rendering…');await renderPdf();loading(false);}});

// ═══════════════════════════════════════════════════════
// KEYBOARD
// ═══════════════════════════════════════════════════════
$(document).on('keydown', e => {
  if(e.key==='v'||e.key==='V'){setTool('select');return;}
  if(e.key==='m'||e.key==='M'){setTool('measure');return;}
  if(e.key==='Escape'){clearMeasure();setTool('select');return;}
  if(e.key==='Delete'||e.key==='Backspace'){
    if(G.selId&&!['INPUT','TEXTAREA'].includes(document.activeElement.tagName)){
      e.preventDefault();removeLogo(G.selId);return;
    }
  }
  if(!G.pdfDoc||!G.selId)return;
  if(['INPUT','TEXTAREA'].includes(document.activeElement.tagName))return;
  const l=selLogo();if(!l)return;
  const s=e.shiftKey?10:1;
  if     (e.key==='ArrowLeft') l.px-=s;
  else if(e.key==='ArrowRight')l.px+=s;
  else if(e.key==='ArrowUp')   l.py-=s;
  else if(e.key==='ArrowDown') l.py+=s;
  else return;
  e.preventDefault();syncIn();updateOverlay(l.id);
});

// ═══════════════════════════════════════════════════════
// SAVE → SERVER
// ═══════════════════════════════════════════════════════
$('#btnSave').on('click', async()=>{
  if(!G.logos.length){toast('Chưa có logo nào','err');return;}
  const payload={
    pdf_name:G.pdfName,
    pdf_width_pts:ri(G.pdfW),pdf_height_pts:ri(G.pdfH),
    logos:G.logos.map((l,i)=>({
      index:i+1, name:l.name,
      x:ri(l.px),y:ri(l.py),w:ri(l.pw),h:ri(l.ph),
      x_mm:+(l.px*PT2MM).toFixed(2),y_mm:+(l.py*PT2MM).toFixed(2),
      w_mm:+(l.pw*PT2MM).toFixed(2),h_mm:+(l.ph*PT2MM).toFixed(2),
      rotation:l.rot,opacity:l.opa,page:1,
    })),
  };
  loading(true,'Đang lưu…');
  try{
    const r=await fetch(`${API}/api/save-placement`,{
      method:'POST',headers:{'Content-Type':'application/json'},
      body:JSON.stringify({pdf_name:payload.pdf_name,logo_name:G.logos.map(l=>l.name).join(', '),pdf_width_pts:payload.pdf_width_pts,pdf_height_pts:payload.pdf_height_pts,placements:payload.logos}),
    });
    const d=await r.json();
    if(!r.ok)throw new Error(d.error);
    showJson(payload);
    toast(`Đã lưu ${G.logos.length} logo ✓`,'ok');
  }catch(e){showJson(payload);toast('Server offline — JSON local','warn');}
  finally{loading(false);}
});

$('#btnLoad').on('click',async()=>{
  try{
    const r=await fetch(`${API}/api/load-placements`);
    const list=await r.json();
    if(!list.length){toast('Chưa có dữ liệu','warn');return;}
    showJson(list[list.length-1]);
    toast('Đã tải placement','ok');
  }catch(e){toast('Server offline','warn');}
});

// ═══════════════════════════════════════════════════════
// EXPORT PDF — all logos
// ═══════════════════════════════════════════════════════
$('#btnExp').on('click',async()=>{
  if(!G.pdfDoc||!G.logos.length){toast('Cần PDF và ít nhất 1 logo!','err');return;}
  loading(true,`Đang ghép ${G.logos.length} logo vào PDF…`);
  try{
    // Browser export via pdf-lib (handles multiple logos)
    await exportBrowser();
    toast(`PDF đã xuất với ${G.logos.length} logo ✓`,'ok');
  }catch(e){toast('Lỗi xuất PDF: '+e.message,'err');console.error(e);}
  finally{loading(false);}
});

async function exportBrowser(){
  const doc=await PDFLib.PDFDocument.load(G.pdfBuf.slice());
  const page=doc.getPages()[0];
  const{width:pw,height:ph}=page.getSize();

  for(const l of G.logos){
    let pngBytes=l.buf instanceof Uint8Array?l.buf:null;
    if(!pngBytes){
      const cv2=document.createElement('canvas');
      const im=await iLoad(l.url);
      cv2.width=im.naturalWidth;cv2.height=im.naturalHeight;
      cv2.getContext('2d').drawImage(im,0,0);
      pngBytes=url2u8(cv2.toDataURL('image/png'));
    }
    const img=await doc.embedPng(pngBytes);
    page.drawImage(img,{
      x:l.px, y:ph-l.py-l.ph,
      width:l.pw, height:l.ph,
      opacity:l.opa,
      rotate:PDFLib.degrees(l.rot),
    });
  }
  dlBlob(new Blob([await doc.save()],{type:'application/pdf'}),
         G.pdfName.replace('.pdf','')+'_logos.pdf');
}

// ═══════════════════════════════════════════════════════
// UTILS
// ═══════════════════════════════════════════════════════
function setupDrop($z,$i,exts,fn){
  $z.on('click',()=>$i.trigger('click'));
  $i.on('change',function(){if(this.files[0])fn(this.files[0]);});
  $z.on('dragover',e=>{e.preventDefault();$z.addClass('drag');});
  $z.on('dragleave drop',()=>$z.removeClass('drag'));
  $z.on('drop',e=>{
    e.preventDefault();
    const f=e.originalEvent.dataTransfer.files[0];if(!f)return;
    if(!exts.includes(f.name.split('.').pop().toLowerCase())){toast('.'+f.name.split('.').pop()+' không hỗ trợ','err');return;}
    fn(f);
  });
}
function fr2url(f){return new Promise((res,rej)=>{const r=new FileReader();r.onload=e=>res(e.target.result);r.onerror=rej;r.readAsDataURL(f);});}
function b64u8(b){const bin=atob(b);const a=new Uint8Array(bin.length);for(let i=0;i<bin.length;i++)a[i]=bin.charCodeAt(i);return a;}
function url2u8(u){return b64u8(u.split(',')[1]);}
function iLoad(s){return new Promise((res,rej)=>{const i=new Image();i.onload=()=>res(i);i.onerror=rej;i.src=s;});}
function dlBlob(blob,name){const u=URL.createObjectURL(blob);const a=document.createElement('a');a.href=u;a.download=name;a.click();setTimeout(()=>URL.revokeObjectURL(u),3000);}
function showJson(o){$('#jbox').text(JSON.stringify(o,null,2)).addClass('on');}
function _fmtSz(b){return b<1048576?(b/1024).toFixed(1)+'KB':(b/1048576).toFixed(1)+'MB';}

// ═══════════════════════════════════════════════════════
// INIT
// ═══════════════════════════════════════════════════════
$(document).ready(function(){
  updBtns();
  $(window).on('resize',drawRulers);
  drawRulers();
  checkGs().then(ping=>{
    if(!ping){
      toast(`⚠ <b>Không kết nối API server</b><br><small>${API}</small>`,'warn');
    }else if(!ping.gs_ok){
      toast(`⚠ <b>GS chưa cài</b> — dùng PNG/JPG thay EPS`,'warn');
    }else{
      toast(`Sẵn sàng — GS ${ping.gs_version} ✓  |  V=Chọn  M=Đo  Del=Xóa logo`,'ok');
    }
  });
});
</script>
</body>
</html>