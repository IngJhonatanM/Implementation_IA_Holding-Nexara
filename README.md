<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Caso — Holding Nexara</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=Instrument+Sans:wght@400;500;600;700&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
:root {
  --bg: #0e0c12;
  --surface: #14101a;
  --surface-2: #1c1624;
  --surface-3: #261e30;
  --ink: #f0eaf8;
  --ink-2: #c4bcd4;
  --ink-3: #8a8296;
  --ink-4: #564e64;
  --line: #2a2238;
  --accent: #c84050;
  --accent-2: #e06070;
  --accent-dim: rgba(200,64,80,0.12);
  --teal: #1a9a8a;
  --teal-dim: rgba(26,154,138,0.15);
  --purple: #9070c0;
  --purple-dim: rgba(144,112,192,0.15);
  --red: #c83040;
  --red-dim: rgba(200,48,64,0.12);
  --green: #40b870;
  --green-dim: rgba(64,184,112,0.12);
  --blue: #6090c8;
  --blue-dim: rgba(96,144,200,0.12);
  --gradient-hero: linear-gradient(160deg, #1a1228 0%, #0e0c12 40%, #120e1a 100%);
  --gradient-accent: linear-gradient(135deg, #c84050 0%, #e06070 100%);
  --font-display: 'DM Serif Display', Georgia, serif;
  --font-body: 'Instrument Sans', system-ui, sans-serif;
  --font-mono: 'JetBrains Mono', monospace;
}
* { box-sizing: border-box; margin: 0; padding: 0; }
html { scroll-behavior: smooth; }
body { background: var(--bg); color: var(--ink-2); font-family: var(--font-body); font-size: 16px; line-height: 1.7; -webkit-font-smoothing: antialiased; }
::selection { background: var(--accent); color: var(--bg); }

/* ── LAYOUT ── */
.container { max-width: 1100px; margin: 0 auto; padding: 0 48px; }
@media (max-width: 768px) { .container { padding: 0 24px; } }

/* ── NAV ── */
nav { position: fixed; top: 0; left: 0; right: 0; z-index: 100; padding: 20px 0; background: rgba(14,12,18,0.88); backdrop-filter: blur(20px); border-bottom: 1px solid var(--line); }
nav .container { display: flex; justify-content: space-between; align-items: center; }
nav .logo { font-family: var(--font-display); font-size: 18px; color: var(--ink); letter-spacing: -0.02em; }
nav .logo em { color: var(--accent); font-style: italic; }
nav .tag { font-size: 11px; font-weight: 600; letter-spacing: 0.1em; text-transform: uppercase; color: var(--ink-3); padding: 5px 12px; border: 1px solid var(--line); border-radius: 999px; }

/* ── HERO ── */
.hero { min-height: 100vh; display: flex; align-items: center; background: var(--gradient-hero); position: relative; overflow: hidden; padding-top: 80px; }
.hero::before { content: ''; position: absolute; top: -200px; right: -200px; width: 600px; height: 600px; background: radial-gradient(circle, rgba(200,64,80,0.06) 0%, transparent 70%); pointer-events: none; }
.hero::after { content: ''; position: absolute; bottom: -100px; left: -100px; width: 400px; height: 400px; background: radial-gradient(circle, rgba(26,154,138,0.05) 0%, transparent 70%); pointer-events: none; }
.hero-content { position: relative; z-index: 1; }
.hero-eyebrow { font-size: 12px; font-weight: 600; letter-spacing: 0.15em; text-transform: uppercase; color: var(--accent); margin: 0 0 24px; display: flex; align-items: center; gap: 12px; }
.hero-eyebrow::before { content: ''; width: 32px; height: 1px; background: var(--accent); }
.hero h1 { font-family: var(--font-display); font-size: clamp(42px, 6vw, 72px); line-height: 1.08; color: var(--ink); margin: 0 0 32px; max-width: 800px; letter-spacing: -0.02em; }
.hero h1 em { color: var(--accent); font-style: italic; }
.hero-desc { font-size: 18px; color: var(--ink-2); max-width: 600px; line-height: 1.7; margin: 0 0 48px; }
.hero-metrics { display: grid; grid-template-columns: repeat(auto-fit, minmax(140px, 1fr)); gap: 1px; background: var(--line); border: 1px solid var(--line); border-radius: 8px; overflow: hidden; max-width: 700px; }
.hero-metric { background: var(--surface); padding: 20px 22px; }
.hero-metric .num { font-family: var(--font-display); font-size: 28px; color: var(--ink); display: block; letter-spacing: -0.01em; }
.hero-metric .lbl { font-size: 11px; color: var(--ink-3); text-transform: uppercase; letter-spacing: 0.08em; font-weight: 600; margin-top: 6px; display: block; }

/* ── SECTIONS ── */
section { padding: 100px 0; }
section + section { border-top: 1px solid var(--line); }
.section-num { font-family: var(--font-mono); font-size: 13px; color: var(--accent); display: flex; align-items: center; gap: 12px; margin: 0 0 16px; font-weight: 500; }
.section-num::after { content: ''; flex: 1; height: 1px; background: var(--line); }
h2 { font-family: var(--font-display); font-size: clamp(28px, 4vw, 40px); color: var(--ink); line-height: 1.15; margin: 0 0 20px; letter-spacing: -0.02em; }
h2 em { color: var(--accent); font-style: italic; }
h3 { font-family: var(--font-display); font-size: 22px; color: var(--ink); margin: 0 0 12px; letter-spacing: -0.01em; }
.section-desc { font-size: 17px; max-width: 640px; margin: 0 0 48px; }

/* ── CARDS ── */
.card { background: var(--surface); border: 1px solid var(--line); border-radius: 8px; padding: 28px 30px; transition: border-color 0.2s; }
.card:hover { border-color: var(--ink-4); }
.card-label { font-size: 10px; font-weight: 700; letter-spacing: 0.12em; text-transform: uppercase; padding: 4px 10px; border-radius: 4px; display: inline-block; margin: 0 0 14px; }
.card-label.teal { background: var(--teal-dim); color: var(--teal); }
.card-label.purple { background: var(--purple-dim); color: var(--purple); }
.card-label.accent { background: var(--accent-dim); color: var(--accent); }
.card-label.red { background: var(--red-dim); color: var(--red); }
.card-label.green { background: var(--green-dim); color: var(--green); }
.card-label.blue { background: var(--blue-dim); color: var(--blue); }

/* ── GRID LAYOUTS ── */
.grid-2 { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; align-items: stretch; }
.grid-2 .card, .grid-3 .card { display: flex; flex-direction: column; }
.grid-3 { display: grid; grid-template-columns: repeat(3, 1fr); gap: 16px; }
@media (max-width: 768px) { .grid-2, .grid-3 { grid-template-columns: 1fr; } }

/* ── TECH STACK BAR ── */
.tech-bar { display: flex; flex-wrap: wrap; gap: 8px; margin: 24px 0 0; }
.tech-pill { font-size: 11px; font-weight: 600; letter-spacing: 0.04em; padding: 5px 12px; border-radius: 4px; background: var(--surface-3); color: var(--ink-3); border: 1px solid var(--line); }

/* ── FLOW DIAGRAM ── */
.flow { display: flex; align-items: center; gap: 0; margin: 40px 0; overflow-x: auto; padding: 12px 0; }
.flow-node { background: var(--surface); border: 1px solid var(--line); border-radius: 8px; padding: 16px 20px; min-width: 150px; text-align: center; flex-shrink: 0; }
.flow-node .icon { font-size: 24px; margin: 0 0 8px; display: block; }
.flow-node .name { font-size: 13px; font-weight: 600; color: var(--ink); display: block; }
.flow-node .sub { font-size: 11px; color: var(--ink-3); display: block; margin-top: 2px; }
.flow-arrow { color: var(--accent); font-size: 20px; padding: 0 8px; flex-shrink: 0; }

/* ── CODE BLOCKS ── */
.code-block { background: var(--surface); border: 1px solid var(--line); border-radius: 8px; overflow: hidden; margin: 24px 0; }
.code-header { padding: 10px 16px; border-bottom: 1px solid var(--line); display: flex; justify-content: space-between; align-items: center; }
.code-header .filename { font-family: var(--font-mono); font-size: 12px; color: var(--ink-3); font-weight: 500; }
.code-header .lang { font-size: 10px; font-weight: 600; letter-spacing: 0.08em; text-transform: uppercase; color: var(--accent); }
.code-body { padding: 16px 20px; font-family: var(--font-mono); font-size: 13px; line-height: 1.7; color: var(--ink-2); overflow-x: auto; white-space: pre; }
.code-body .comment { color: var(--ink-4); }
.code-body .keyword { color: var(--accent); }
.code-body .string { color: var(--teal); }
.code-body .func { color: var(--purple); }

/* ── KPI SHOWCASE ── */
.kpi-showcase { display: grid; grid-template-columns: repeat(auto-fit, minmax(160px, 1fr)); gap: 1px; background: var(--line); border: 1px solid var(--line); border-radius: 8px; overflow: hidden; margin: 32px 0; }
.kpi-item { background: var(--surface); padding: 22px 24px; }
.kpi-item .val { font-family: var(--font-display); font-size: 30px; color: var(--ink); letter-spacing: -0.01em; }
.kpi-item .val.green { color: var(--green); }
.kpi-item .val.red { color: var(--red); }
.kpi-item .label { font-size: 11px; color: var(--ink-3); text-transform: uppercase; letter-spacing: 0.08em; font-weight: 600; margin-top: 6px; }

/* ── TIMELINE ── */
.timeline { position: relative; padding-left: 32px; margin: 32px 0; }
.timeline::before { content: ''; position: absolute; left: 6px; top: 8px; bottom: 8px; width: 1px; background: var(--line); }
.tl-item { position: relative; padding: 0 0 32px; }
.tl-item:last-child { padding-bottom: 0; }
.tl-item::before { content: ''; position: absolute; left: -29px; top: 8px; width: 9px; height: 9px; border-radius: 50%; background: var(--accent); border: 2px solid var(--bg); }
.tl-item .phase { font-size: 11px; font-weight: 700; letter-spacing: 0.1em; text-transform: uppercase; color: var(--accent); margin: 0 0 6px; }
.tl-item .title { font-family: var(--font-display); font-size: 18px; color: var(--ink); margin: 0 0 6px; }
.tl-item .desc { font-size: 14px; color: var(--ink-3); }

/* ── SCREENSHOT MOCKUP ── */
.screenshot { background: var(--surface); border: 1px solid var(--line); border-radius: 12px; overflow: hidden; margin: 40px 0; box-shadow: 0 20px 60px -20px rgba(0,0,0,0.5); }
.screenshot .bar { height: 36px; background: var(--surface-2); border-bottom: 1px solid var(--line); display: flex; align-items: center; padding: 0 14px; gap: 8px; }
.screenshot .bar .dot { width: 10px; height: 10px; border-radius: 50%; }
.screenshot .bar .dot.r { background: #d05050; }
.screenshot .bar .dot.y { background: #c09030; }
.screenshot .bar .dot.g { background: #40a860; }
.screenshot .bar .url { margin-left: 12px; font-family: var(--font-mono); font-size: 11px; color: var(--ink-4); background: var(--surface); padding: 4px 14px; border-radius: 4px; flex: 1; max-width: 400px; }
.screenshot .content { padding: 32px; min-height: 300px; display: flex; flex-direction: column; gap: 20px; }
.ss-kpis { display: grid; grid-template-columns: repeat(5, 1fr); gap: 10px; }
.ss-kpi { background: var(--surface-2); border-radius: 6px; padding: 14px 16px; }
.ss-kpi .lbl { font-size: 9px; color: var(--ink-4); text-transform: uppercase; letter-spacing: 0.08em; font-weight: 600; }
.ss-kpi .val { font-family: var(--font-display); font-size: 18px; color: var(--ink); margin-top: 4px; }
.ss-chart { background: var(--surface-2); border-radius: 6px; padding: 20px; flex: 1; display: flex; align-items: flex-end; gap: 12px; }
.ss-bar { border-radius: 4px 4px 0 0; min-width: 40px; flex: 1; }
@media (max-width: 768px) { .ss-kpis { grid-template-columns: repeat(3, 1fr); } }

/* ── TABLE ── */
table.specs { width: 100%; border-collapse: collapse; font-size: 14px; }
table.specs th { text-align: left; font-size: 10px; text-transform: uppercase; letter-spacing: 0.08em; color: var(--ink-4); font-weight: 600; padding: 10px 14px; border-bottom: 1px solid var(--line); }
table.specs td { padding: 12px 14px; border-bottom: 1px solid var(--line); color: var(--ink-2); }
table.specs td:first-child { color: var(--ink); font-weight: 500; }
table.specs tr:hover td { background: var(--surface-2); }

/* ── CALLOUT ── */
.callout { border-left: 3px solid var(--accent); padding: 20px 24px; background: var(--accent-dim); border-radius: 0 6px 6px 0; margin: 32px 0; }
.callout p { font-size: 15px; color: var(--ink-2); margin: 0; }
.callout strong { color: var(--ink); }

/* ── FOOTER ── */
footer { padding: 60px 0; border-top: 1px solid var(--line); }
footer .container { display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 16px; }
footer .left { font-family: var(--font-display); font-size: 16px; color: var(--ink); }
footer .left em { color: var(--accent); font-style: italic; }
footer .right { font-size: 12px; color: var(--ink-4); }

/* ── ANIMATIONS ── */
@keyframes fadeUp { from { opacity: 0; transform: translateY(20px); } to { opacity: 1; transform: translateY(0); } }
.animate { opacity: 0; animation: fadeUp 0.6s ease forwards; }
.delay-1 { animation-delay: 0.1s; }
.delay-2 { animation-delay: 0.2s; }
.delay-3 { animation-delay: 0.3s; }
.delay-4 { animation-delay: 0.4s; }
.delay-5 { animation-delay: 0.5s; }
</style>
</head>
<body>

<nav>
  <div class="container">
    <div class="logo">Solucion · <em>Holding Nexara</em></div>
    <div class="tag">Orquestación De Datos Distribuidos Con Claude</div>
  </div>
</nav>

<!-- ═══════════════════ HERO ═══════════════════ -->
<section class="hero">
  <div class="container">
    <div class="hero-content">
      <p class="hero-eyebrow animate">Caso — Holding Nexara</p>
      <h1 class="animate delay-1">Orquestación de <em>datos en tiempo real</em> para un holding de 5 empresas</h1>
      <p class="hero-desc animate delay-2">Diseñé e implementé un sistema de inteligencia operativa que consolida datos financieros de 5 empresas usando Claude AI como agente autónomo, MCPs como puentes de datos hacia el cloud donde estan los archivos y la infraestructura Docker/Ubuntu personalizada para conectar el ERP contable, y Live Artifacts como interfaz para la presentacion de datos y toma de decisiones del CEO.</p>
      
      <div class="hero-metrics animate delay-3">
        <div class="hero-metric"><span class="num">5</span><span class="lbl">Empresas</span></div>
        <div class="hero-metric"><span class="num">820</span><span class="lbl">Hojas Excel</span></div>
        <div class="hero-metric"><span class="num">$11.2M</span><span class="lbl">Ventas trazadas</span></div>
        <div class="hero-metric"><span class="num">$19.4M</span><span class="lbl">CxP monitoreado</span></div>
        <div class="hero-metric"><span class="num">7</span><span class="lbl">Skills creados</span></div>
      </div>
    </div>
  </div>
</section>

<!-- ═══════════════════ CONTEXT ═══════════════════ -->
<section>
  <div class="container">
    <p class="section-num">01 <span></span></p>
    <h2>El <em>cliente</em></h2>
    <p class="section-desc">Holding Nexara es un grupo empresarial venezolano con operaciones en azúcar, aceite, arroz, pasta y refinación. Cada empresa opera de forma independiente con sus propios Excel operativos, pero el CEO necesita visión consolidada para decisiones.</p>
    
    <div class="grid-3">
      <div class="card animate">
        <span class="card-label accent">Matriz</span>
        <h3>Nexara Capital</h3>
        <p style="font-size:14px;color:var(--ink-3)">Ventas de azúcar. $6.2M en resultado acumulado. Archivo más rico: 290 hojas, 6 MB. Concentra el 74% de las ventas del grupo.</p>
      </div>
      <div class="card animate delay-1">
        <span class="card-label teal">Refinación</span>
        <h3>Aldra Alimentos</h3>
        <p style="font-size:14px;color:var(--ink-3)">Maquila y refinación de aceite. Operación industrial con proveedores internacionales (Brasil). $480K en activos fijos.</p>
      </div>
      <div class="card animate delay-2">
        <span class="card-label purple">Empaque</span>
        <h3>Pacora Grains</h3>
        <p style="font-size:14px;color:var(--ink-3)">Empaque de azúcar, arroz y cereales. Archivo más pesado: 24 MB, 155 hojas. $4.1M en inventario de arroz.</p>
      </div>
      <div class="card animate delay-3">
        <span class="card-label red">Central</span>
        <h3>Cendral Refinería</h3>
        <p style="font-size:14px;color:var(--ink-3)">Central azucarero. $8.1M en inventario (crudo + refinada). Toda la operación financiada por terceros.</p>
      </div>
      <div class="card animate delay-4">
        <span class="card-label green">Producción</span>
        <h3>Vitapast</h3>
        <p style="font-size:14px;color:var(--ink-3)">Producción de pastas. En fase preoperativa. Maquinaria valorada en $640K. Sin saldo bancario propio.</p>
      </div>
    </div>
  </div>
</section>

<!-- ═══════════════════ PROBLEM ═══════════════════ -->
<section>
  <div class="container">
    <p class="section-num">02 <span></span></p>
    <h2>El <em>problema</em></h2>
    <p class="section-desc">Hay un complejo entramado de un grupo empresarial donde Nexara actúa como la entidad matriz y accionista principal que vincula diversas unidades de negocio especializadas. Cada empresa opera de forma independiente según su rubro, a pesar de esta autonomía operativa, la estructura se mantiene unida por una gestión financiera que busca conciliar los datos operativos en tiempo real con los registros administrativos formales. El objetivo fundamental de esta organización es alcanzar una precisión analítica en los costos y la rentabilidad, permitiendo que la dirección tome decisiones estratégicas inmediatas basadas en la comparación exacta entre los inventarios físicos y los estados financieros.</p>
    
    <div class="grid-2">
      <div class="card">
        <h3 style="color:var(--red)">Antes</h3>
        <p style="font-size:14px;color:var(--ink-3);margin-top:8px"><strong style="color:var(--ink-2)">Operativo:</strong> Cada empresa mantenía su propio Excel con estructura diferente. Para ver el consolidado, alguien abría los 5 archivos, copiaba números a mano y armaba un resumen. Proceso manual, propenso a errores, que tomaba horas.</p>
        <p style="font-size:14px;color:var(--ink-3);margin-top:12px"><strong style="color:var(--ink-2)">Contable:</strong> El ERP Profit (SQL Server) estaba completamente aislado. Nadie podía consultarlo sin acceso directo al servidor Windows. Los cierres contables llegaban tarde, sin cruce con la data operativa, sin alertas de discrepancia.</p>
        <div class="tech-bar" style="margin-top:16px">
          <span class="tech-pill">5 Excel aislados</span>
          <span class="tech-pill">ERP inaccesible</span>
          <span class="tech-pill">Sin conciliación</span>
          <span class="tech-pill">Proceso manual</span>
        </div>
      </div>
      <div class="card">
        <h3 style="color:var(--green)">Después</h3>
        <p style="font-size:14px;color:var(--ink-3);margin-top:8px"><strong style="color:var(--ink-2)">Operativo:</strong> Claude lee los 5 Excel desde Google Drive vía MCP, los procesa en memoria y genera un dashboard interactivo con 7 vistas, filtros por empresa, búsqueda global y 1,200+ partidas detalladas. Automático, diario, sin intervención.</p>
        <p style="font-size:14px;color:var(--ink-3);margin-top:12px"><strong style="color:var(--ink-2)">Contable:</strong> VM Ubuntu + Docker expone el ERP Profit como MCP. Claude consulta el Libro Mayor desde cualquier laptop autorizada a través de un túnel cifrado. Conversión Bs→USD automática con tasa BCV. Alertas de discrepancia operativo vs contable.</p>
        <div class="tech-bar" style="margin-top:16px">
          <span class="tech-pill">MCP Google Drive</span>
          <span class="tech-pill">MCP SQL Server</span>
          <span class="tech-pill">VM + Docker</span>
          <span class="tech-pill">Conciliación automática</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ═══════════════════ ROADMAP ═══════════════════ -->
<section>
  <div class="container">
    <p class="section-num">03 <span></span></p>
    <h2><em>Roadmap</em> del proyecto</h2>
    <p class="section-desc">El sistema está diseñado para ejecutar los conectores en el centro de datos del cliente que es donde reside la data, así el "camino" que recorre hasta los documentos y la base de datos el conector MCP (En docker & Docker Compose para que sean portables y fáciles de gestionar si fallan) interno es ultra rápido. Abres Claude en cualquier laptop autorizada, se conecta por red segura (mediante VPN, esto garantiza que la data nunca esté expuesta a internet público manteniendo privacidad )a la IP de la VM donde están los MCPs. Así, aunque apagues tu laptop, la configuración de acceso a Profit y Excel sigue "viva" y lista en la infraestructura del servidor.</p>
    
    <div class="timeline">
      <div class="tl-item">
        <div class="phase">Fase 1 — Completada</div>
        <div class="title">Dashboard Excel (Operativo)</div>
        <div class="desc">Consolidación de los 5 Excel vía Google Drive MCP. Dashboard con 7 vistas, filtros, búsqueda. Actualización diaria automática vía /schedule.</div>
      </div>
      <div class="tl-item">
        <div class="phase">Fase 2 — Completada</div>
        <div class="title">Dashboard Profit (Contable)</div>
        <div class="desc">VM Ubuntu + Docker con MCP custom (profit-sqlserver). 57 bases de datos, la principal de 103 GB. túnel cifrado (VPN/Tailscale/SSH) para conectividad segura desde cualquier laptop autorizada. 4 skills especializados (DB_Router, currency_normalizer, Analista Financiero, Fiscal_Monitor). Vista contable/administrativa en desarrollo.</div>
      </div>
      <div class="tl-item">
        <div class="phase">Fase 3 — En progreso</div>
        <div class="title">Dashboard General (Conciliación)</div>
        <div class="desc">Cruce automático de datos operativos (Excel) vs contables (Profit). Alertas por discrepancia: >5% rojo, 1-5% amarillo, <1% OK. Vista CEO consolidada.</div>
      </div>
    </div>
  </div>
</section>


<!-- ═══════════════════ ARCHITECTURE ═══════════════════ -->
<section>
  <div class="container">
    <p class="section-num">04 <span></span></p>
    <h2>Arquitectura <em>técnica</em></h2>

    <h3 style="margin-top:40px">Datos Operativos Excel</h3>
    <p class="section-desc"> La VM Ubuntu hace mount CIFS de la carpeta de red compartida donde estan los archivos y rclone realiza sync de los Excel a Google Drive, los datos fluyen desde Google Drive hasta el dashboard sin tocar disco.</p>
    
    <div class="flow">
      <div class="flow-node"><span class="icon">📁</span><span class="name">rclone</span><span class="sub">Sync automático</span></div>
      <span class="flow-arrow">→</span>
      <div class="flow-node"><span class="icon">☁️</span><span class="name">Google Drive</span><span class="sub">5 archivos .xlsx</span></div>
      <span class="flow-arrow">→</span>
      <div class="flow-node" style="border-color:var(--accent)"><span class="icon">🔌</span><span class="name">MCP</span><span class="sub">google-drive</span></div>
      <span class="flow-arrow">→</span>
      <div class="flow-node" style="border-color:var(--teal)"><span class="icon">🧠</span><span class="name">Claude Agent</span><span class="sub">Cowork + Skills</span></div>
      <span class="flow-arrow">→</span>
      <div class="flow-node" style="border-color:var(--purple)"><span class="icon">📊</span><span class="name">Live Artifact</span><span class="sub">Dashboard HTML</span></div>
      <span class="flow-arrow">→</span>
      <div class="flow-node"><span class="icon">👔</span><span class="name">CEO</span><span class="sub">Claude Teams</span></div>
    </div>

    <div class="callout">
      <p><strong>Principio arquitectónico:</strong> TODO EN MEMORIA. Los archivos Excel nunca se descargan al disco local. El MCP de Google Drive los lee directamente, Claude los procesa en memoria (io.BytesIO), sin descargas locales, sin bases de datos intermedias. Los datos fluyen desde Google Drive hasta el dashboard sin tocar disco.</p> y el output es un Live Artifact que se presenta al usuario. Lo único que persiste a disco son los logs de auditoría.</p>
    </div>
    
    <h3 style="margin-top:40px">Registros Administrativos ERP Profit</h3>
    <p class="section-desc"> El ERP contable (Profit) corre sobre <strong style="color:var(--ink)">SQL Server Enterprise en Windows</strong>. Para que Claude pudiera consultarlo de forma segura y controlada, diseñé un stack de contenedores sobre una VM Ubuntu que actúa como intermediario, que permite acceder de forma segura al servidor de producción sin modificarlo. El acceso funciona desde cualquier laptop autorizada a través de un túnel cifrado los datos sensibles nunca viajan por internet público.</p>
    <div class="flow">
      <div class="flow-node" style="border-color:var(--accent)">
        <span class="icon">💻</span>
        <span class="name">Laptop autorizada</span>
        <span class="sub">Claude Desktop</span>
      </div>
      <span class="flow-arrow">→</span>
      <div class="flow-node" style="border-color:var(--red)">
        <span class="icon">🔐</span>
        <span class="name">Túnel cifrado</span>
        <span class="sub">VPN / Tailscale / SSH</span>
      </div>
      <span class="flow-arrow">→</span>
      <div class="flow-node" style="border-color:var(--teal)">
        <span class="icon">🐧</span>
        <span class="name">VM Ubuntu</span>
        <span class="sub">Servidor de MCPs</span>
      </div>
      <span class="flow-arrow">→</span>
      <div class="flow-node" style="border-color:var(--purple)">
        <span class="icon">🐳</span>
        <span class="name">Docker</span>
        <span class="sub">mcp-sqlserver</span>
      </div>
      <span class="flow-arrow">→</span>
      <div class="flow-node">
        <span class="icon">🗄️</span>
        <span class="name">SQL Server</span>
        <span class="sub">Profit ERP · Windows</span>
      </div>
    </div>

    <div class="callout">
      <p><strong>Privacidad por diseño:</strong> Los datos contables del cliente nunca viajan por internet público. Solo los fragmentos necesarios para el análisis se transmiten al modelo de Claude a través del túnel cifrado. La VM Ubuntu queda siempre activa en la red del cliente — apagar la laptop del operador no interrumpe la disponibilidad de los MCPs.</p>
    </div>

    <div class="grid-2" style="margin-top:24px">
      <div class="card">
        <span class="card-label teal">Infraestructura</span>
        <h3>VM Ubuntu + Docker</h3>
        <p style="font-size:14px;color:var(--ink-3);margin:8px 0 16px">Levanté una VM Ubuntu con Docker donde desplegué el contenedor del MCP de SQL Server (<code style="font-family:var(--font-mono);font-size:12px;color:var(--accent)">mcp-mssqlserver</code>). Este contenedor expone las herramientas <code style="font-family:var(--font-mono);font-size:12px;color:var(--accent)">list_databases</code>, <code style="font-family:var(--font-mono);font-size:12px;color:var(--accent)">list_tables</code>, <code style="font-family:var(--font-mono);font-size:12px;color:var(--accent)">describe_table</code> y <code style="font-family:var(--font-mono);font-size:12px;color:var(--accent)">query</code> al agente de Claude vía el protocolo MCP estándar. La VM queda siempre activa — los MCPs siguen disponibles aunque la laptop del operador esté apagada.</p>
        <div class="tech-bar">
          <span class="tech-pill">Ubuntu Server</span>
          <span class="tech-pill">Docker</span>
          <span class="tech-pill">mcp-mssqlserver</span>
          <span class="tech-pill">Node.js</span>
        </div>
      </div>
      <div class="card">
        <span class="card-label red">Acceso seguro</span>
        <h3>Túnel cifrado + solo lectura</h3>
        <p style="font-size:14px;color:var(--ink-3);margin:8px 0 16px">Claude Desktop en cualquier laptop autorizada se conecta a la IP de la VM a través de un <strong style="color:var(--ink)">túnel cifrado</strong> (VPN / Tailscale / SSH Reverse Tunnel). Los datos sensibles del cliente nunca viajan por internet público — solo los fragmentos necesarios para el análisis se envían al modelo a través del túnel. El usuario <code style="font-family:var(--font-mono);font-size:12px;color:var(--accent)">claude_auditoria</code> tiene permisos estrictamente limitados a SELECT.</p>
        <div class="tech-bar">
          <span class="tech-pill">VPN / Tailscale / SSH</span>
          <span class="tech-pill">SQL Server Enterprise</span>
          <span class="tech-pill">claude_auditoria</span>
          <span class="tech-pill">Solo SELECT</span>
        </div>
      </div>
    </div>

    <h3 style="margin-top:40px">Stack técnico</h3>

    <!-- Stack Profit -->
    <div style="display:flex;align-items:center;gap:12px;margin:16px 0 10px">
      <span style="padding:3px 10px;background:var(--purple-dim);color:var(--purple);font-size:11px;font-weight:700;letter-spacing:0.1em;text-transform:uppercase;border-radius:4px">🗄️ Stack Profit · SQL Server</span>
      <span style="height:1px;flex:1;background:var(--line)"></span>
    </div>
    <table class="specs" style="margin-bottom:24px">
      <thead><tr><th>Componente</th><th>Tecnología</th><th>Rol</th></tr></thead>
      <tbody>
        <tr><td>VM Ubuntu</td><td>Servidor dedicado para el stack MCP</td><td>Aislamiento: el agente nunca toca directamente el SQL Server</td></tr>
        <tr><td>Fuente contable</td><td>Profit-Sqlserver</td><td>Lectura de base contable vía VM Ubuntu + Docker</td></tr>
        <tr><td>Infraestructura</td><td>Ubuntu VM + Docker + túnel cifrado</td><td>Contenedor MCP siempre activo · acceso seguro desde cualquier laptop autorizada</td></tr>
        <tr><td>Skills Profit</td><td>DB_Router · currency_normalizer · Analista · Fiscal_Monitor</td><td>Pipeline contable (SQL Server)</td></tr>
      </tbody>
    </table>

    <!-- Stack Excel -->
    <div style="display:flex;align-items:center;gap:12px;margin:0 0 10px">
      <span style="padding:3px 10px;background:var(--teal-dim);color:var(--teal);font-size:11px;font-weight:700;letter-spacing:0.1em;text-transform:uppercase;border-radius:4px">📊 Stack Excel · Google Drive</span>
      <span style="height:1px;flex:1;background:var(--line)"></span>
    </div>
    <table class="specs">
      <thead><tr><th>Componente</th><th>Tecnología</th><th>Rol</th></tr></thead>
      <tbody>
        <tr><td>Sync operativo</td><td>rclone (carpeta SMB → Google Drive)</td><td>Sincronización automática sin cambiar flujo del cliente</td></tr>
        <tr><td>Fuente operativa</td><td>Google Drive MCP</td><td>Lectura directa de Excel operativos en memoria</td></tr>
        <tr><td>Skills Excel</td><td>drive-analyzer · excel-balance-parser · dashboard-ui</td><td>Pipeline operativo (Google Drive)</td></tr>
        <tr><td>Agente</td><td>Claude Cowork + Scheduled Tasks</td><td>Orquestación autónoma del pipeline completo</td></tr>
        <tr><td>Dashboard</td><td>HTML + CSS + Chart.js (Live Artifact)</td><td>Interfaz interactiva con 7 vistas · actualización diaria</td></tr>
        <tr><td>Auditoría</td><td>change_log.csv + snapshot.json</td><td>Trazabilidad y detección de anomalías</td></tr>
        <tr><td>Equipo</td><td>Claude Teams</td><td>Acceso compartido · CEO + equipo contable</td></tr>
      </tbody>
    </table>
  </div>
</section>

<!-- ═══════════════════ SKILLS ═══════════════════ -->
<section>
  <div class="container">
    <p class="section-num">05 <span></span></p>
    <h2>Los <em>Skills</em> — inteligencia reutilizable</h2>
    <p class="section-desc">Diseñé 7 skills como documentos Markdown que codifican el conocimiento adquirido. 3 para el pipeline Excel (operativo) y 4 para el pipeline Profit (contable). El agente los lee al inicio de cada sesión y ejecuta los procesos sin asistencia.</p>
    
    <!-- SKILLS EXCEL -->
    <div style="display:flex;align-items:center;gap:12px;margin:0 0 20px">
      <span style="padding:4px 14px;background:var(--teal-dim);color:var(--teal);font-size:11px;font-weight:700;letter-spacing:0.1em;text-transform:uppercase;border-radius:4px">📊 Pipeline Excel · Google Drive</span>
      <span style="height:1px;flex:1;background:var(--line)"></span>
    </div>
    <div class="grid-3" style="margin-bottom:40px">
      <div class="card" style="border-top:2px solid var(--teal)">
        <span class="card-label teal">Skill 1 · Excel</span>
        <h3>drive-analyzer.md</h3>
        <p style="font-size:14px;color:var(--ink-3);margin:8px 0 16px">Cómo buscar, validar y leer los 5 archivos de Drive. Incluye la estrategia de lectura por empresa (read vs download), validación de sync de rclone, y manejo de errores.</p>
        <div class="code-block">
          <div class="code-header"><span class="filename">Estrategia de lectura</span><span class="lang">Config</span></div>
          <div class="code-body"><span class="comment"># Optimización de tokens por empresa</span>
Fe Master (6 MB)  → <span class="func">read_file_content</span>
TAO (2.3 MB)      → <span class="func">read_file_content</span>
Pacora Grains (24 MB)   → <span class="keyword">download</span> + <span class="func">BytesIO</span>
Cendral Refinería (2 MB)   → <span class="func">read_file_content</span>
Vitapast (1.7 MB) → <span class="func">read_file_content</span></div>
        </div>
      </div>
      <div class="card">
        <span class="card-label purple">Skill 2</span>
        <h3>excel-balance-parser.md</h3>
        <p style="font-size:14px;color:var(--ink-3);margin:8px 0 16px">El corazón técnico. Define el mapa exacto de columnas por empresa (descubierto por ingeniería inversa), los patrones regex para ventas, y la clasificación de productos.</p>
        <div class="code-block">
          <div class="code-header"><span class="filename">Mapa de columnas</span><span class="lang">Descubrimiento</span></div>
          <div class="code-body"><span class="comment"># Cada empresa usa columnas diferentes</span>
<span class="string">Nexara Capital</span>: concepto=<span class="keyword">B(1)</span> valor=<span class="keyword">E(4)</span>
<span class="string">Aldra Alimentos</span>: concepto=<span class="keyword">B(1)</span> valor=<span class="keyword">D(3)</span>
<span class="string">Pacora Grains</span>:      concepto=<span class="keyword">D(3)</span> valor=<span class="keyword">G(6)</span>
<span class="string">Cendral Refinería</span>:      concepto=<span class="keyword">B(1)</span> valor=<span class="keyword">D(3)</span>
<span class="string">Vitapast</span>:    concepto=<span class="keyword">B(1)</span> valor=<span class="keyword">D(3)</span></div>
        </div>
      </div>
      <div class="card">
        <span class="card-label accent">Skill 3</span>
        <h3>dashboard-ui.md</h3>
        <p style="font-size:14px;color:var(--ink-3);margin:8px 0 16px">Fuente de verdad visual. Define los 26 colores exactos (light + dark mode), tipografía, componentes, estructura del dataset JSON, y el protocolo de actualización.</p>
        <div class="code-block">
          <div class="code-header"><span class="filename">Design tokens</span><span class="lang">CSS</span></div>
          <div class="code-body"><span class="keyword">--bg</span>: <span class="string">#faf8f3</span>   <span class="comment">/* crema cálido */</span>
<span class="keyword">--accent</span>: <span class="string">#8b5a2b</span> <span class="comment">/* marrón tierra */</span>
<span class="keyword">--pos</span>: <span class="string">#2e7d4f</span>    <span class="comment">/* verde ganancia */</span>
<span class="keyword">--neg</span>: <span class="string">#b8442e</span>    <span class="comment">/* rojo deuda */</span>
<span class="func">Font</span>: Fraunces (serif) + Inter (sans)
<span class="func">Charts</span>: Chart.js · 11 colores · cutout 58%</div>
        </div>
      </div>
    </div>

    <!-- SKILLS PROFIT -->
    <div style="display:flex;align-items:center;gap:12px;margin:40px 0 20px">
      <span style="padding:4px 14px;background:var(--purple-dim);color:var(--purple);font-size:11px;font-weight:700;letter-spacing:0.1em;text-transform:uppercase;border-radius:4px">🗄️ Pipeline Profit · SQL Server</span>
      <span style="height:1px;flex:1;background:var(--line)"></span>
    </div>
    <div class="grid-2" style="margin-bottom:16px">
      <div class="card" style="border-top:2px solid var(--purple)">
        <span class="card-label purple">Skill 4 · Profit</span>
        <h3>Profit_DB_Router.md</h3>
        <p style="font-size:14px;color:var(--ink-3);margin:8px 0 16px">El ERP tiene una base de datos por empresa con nombres no intuitivos. Este skill mapea cada empresa a su BD correcta y detecta el patrón de nombres para enrutar automáticamente sin intervención.</p>
        <div class="code-block">
          <div class="code-header"><span class="filename">Mapa empresa → BD</span><span class="lang">Router</span></div>
          <div class="code-body"><span class="comment"># Routing automático por empresa</span>
<span class="string">Nexara Capital</span>  → <span class="keyword">NEXARA02_N</span>
<span class="string">Aldra Alimentos</span> → <span class="keyword">ALDRA01_A</span>
<span class="string">Pacora Grains</span>   → <span class="keyword">PACORA02_N</span>
<span class="string">Cendral Ref.</span>    → <span class="keyword">CENDRAL01_C</span>
<span class="string">Vitapast</span>        → <span class="keyword">VITAPAST02_A</span></div>
        </div>
      </div>
      <div class="card" style="border-top:2px solid var(--purple)">
        <span class="card-label purple">Skill 5 · Profit</span>
        <h3>profit_currency_unit_normalizer.md</h3>
        <p style="font-size:14px;color:var(--ink-3);margin:8px 0 16px">Profit registra en Bolívares venezolanos (Bs). Este skill aplica la tasa BCV oficial del día sobre todos los saldos antes de cualquier cálculo. Incluye manejo de tasas históricas y fuente de respaldo.</p>
        <div class="code-block">
          <div class="code-header"><span class="filename">Normalización de moneda</span><span class="lang">Lógica</span></div>
          <div class="code-body"><span class="comment"># Conversión Bs → USD</span>
saldo_usd = saldo_bs / <span class="func">tasa_bcv_hoy</span>()
<span class="comment"># Fuentes de tasa:</span>
<span class="keyword">1.</span> <span class="string">BCV oficial</span> (primario)
<span class="keyword">2.</span> <span class="string">Dolartoday</span> (respaldo)
<span class="keyword">3.</span> <span class="string">Manual</span> si no hay red</div>
        </div>
      </div>
    </div>
    <div class="grid-2">
      <div class="card" style="border-top:2px solid var(--purple)">
        <span class="card-label purple">Skill 6 · Profit</span>
        <h3>Analista Financiero General (Profit).md</h3>
        <p style="font-size:14px;color:var(--ink-3);margin:8px 0 16px">Define cómo consultar el Libro Mayor: qué tablas contienen saldos, cómo agregar por cuenta contable, cómo filtrar por período fiscal. Es el equivalente contable del excel-balance-parser.</p>
        <div class="tech-bar">
          <span class="tech-pill">Libro Mayor</span>
          <span class="tech-pill">Cuentas contables</span>
          <span class="tech-pill">Períodos fiscales</span>
          <span class="tech-pill">Queries SQL</span>
        </div>
      </div>
      <div class="card" style="border-top:2px solid var(--purple)">
        <span class="card-label purple">Skill 7 · Profit</span>
        <h3>Profit_Fiscal_Monitor.md</h3>
        <p style="font-size:14px;color:var(--ink-3);margin:8px 0 16px">Vigilancia fiscal: detecta asientos sin contrapartida, saldos negativos incorrectos y discrepancias entre mayor y movimientos del período. Primera capa de auditoría antes de la conciliación cruzada.</p>
        <div class="tech-bar">
          <span class="tech-pill">Auditoría</span>
          <span class="tech-pill">Alertas fiscales</span>
          <span class="tech-pill">Mayor vs movimientos</span>
          <span class="tech-pill">Cierres incompletos</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ═══════════════════ DISCOVERIES ═══════════════════ -->
<section>
  <div class="container">
    <p class="section-num">07 <span></span></p>
    <h2>Hallazgos <em>técnicos</em></h2>
    <p class="section-desc">Durante la ingeniería inversa de los archivos Excel y la exploración del ERP Profit encontré anomalías en ambas fuentes que impactan la fiabilidad del análisis. Sin resolverlos, cualquier consolidación automática habría producido datos incorrectos.</p>

    <div style="display:flex;align-items:center;gap:12px;margin:0 0 16px">
      <span style="padding:3px 10px;background:var(--teal-dim);color:var(--teal);font-size:11px;font-weight:700;letter-spacing:0.1em;text-transform:uppercase;border-radius:4px">📊 Pipeline Excel / Google Drive</span>
    </div>
    <div style="display:grid;grid-template-columns:1fr 1fr;gap:16px;margin-bottom:32px;align-items:start">
      <div class="card" style="height:100%">
        <span class="card-label red">Anomalía · Excel</span>
        <h3>Hojas de ventas duplicadas</h3>
        <p style="font-size:14px;color:var(--ink-3);margin-top:8px">Las hojas "ventas mayo", "tabla mayo" y "MAYO" estaban duplicadas idénticamente en los 5 archivos — todas mostraban la misma cifra. Eran plantillas vacías, no datos reales. La fuente correcta era el DIARIO, descubierta por inspección manual.</p>
      </div>
      <div class="card" style="height:100%">
        <span class="card-label red">Anomalía · Excel</span>
        <h3>Pacora Grains sin fechas en DIARIO</h3>
        <p style="font-size:14px;color:var(--ink-3);margin-top:8px">El DIARIO de Pacora Grains no tiene columna de fecha. Solo se puede agregar por categoría de producto, no por período temporal. Requirió un parser alternativo sin dimensión de tiempo.</p>
      </div>
      <div class="card" style="height:100%">
        <span class="card-label accent">Descubrimiento · Excel</span>
        <h3>Columnas variables por empresa</h3>
        <p style="font-size:14px;color:var(--ink-3);margin-top:8px">Cada empresa usa columnas diferentes para el mismo concepto financiero. Pacora Grains tiene el concepto en col D y el valor en col G, mientras las demás usan B y D/E. Mapeado por ingeniería inversa fila por fila.</p>
      </div>
      <div class="card" style="height:100%">
        <span class="card-label accent">Descubrimiento · Excel</span>
        <h3>Archivo inflado 10x por error de formato</h3>
        <p style="font-size:14px;color:var(--ink-3);margin-top:8px">Pacora Grains (24 MB) tiene hojas que Excel reporta como 1,048,576 filas pero solo las primeras ~150 contienen datos. El parser debía limitarse a 1,500 filas para no agotar la memoria.</p>
      </div>
    </div>

    <div style="display:flex;align-items:center;gap:12px;margin:32px 0 16px">
      <span style="padding:3px 10px;background:var(--purple-dim);color:var(--purple);font-size:11px;font-weight:700;letter-spacing:0.1em;text-transform:uppercase;border-radius:4px">🗄️ Pipeline Profit / SQL Server</span>
    </div>
    <div style="display:grid;grid-template-columns:1fr 1fr;gap:16px;align-items:start">
      <div class="card" style="height:100%">
        <span class="card-label red">Anomalía · Profit</span>
        <h3>57 bases con nombres no intuitivos</h3>
        <p style="font-size:14px;color:var(--ink-3);margin-top:8px">El servidor tiene 57 bases de datos activas cuyos nombres no corresponden a los nombres comerciales de las empresas. Sin un mapa de routing, el agente consultaría la base incorrecta. Solución: el skill Profit_DB_Router.</p>
      </div>
      <div class="card" style="height:100%">
        <span class="card-label red">Anomalía · Profit</span>
        <h3>Monedas mixtas sin normalizar</h3>
        <p style="font-size:14px;color:var(--ink-3);margin-top:8px">Profit registra en Bolívares (Bs) e implícitamente en USD según el tipo de operación. Sin conversión previa, los saldos consolidados eran completamente incoherentes. Se diseñó currency_normalizer con fuente BCV primaria y respaldo manual.</p>
      </div>
      <div class="card" style="height:100%">
        <span class="card-label accent">Descubrimiento · Profit</span>
        <h3>Base principal de 103 GB</h3>
        <p style="font-size:14px;color:var(--ink-3);margin-top:8px">La base principal supera los 103 GB. No se puede cargar completa en contexto. El agente debe hacer queries quirúrgicas. El skill Analista Financiero define exactamente qué tablas y columnas consultar.</p>
      </div>
      <div class="card" style="height:100%">
        <span class="card-label accent">Descubrimiento · Profit</span>
        <h3>Asientos sin contrapartida</h3>
        <p style="font-size:14px;color:var(--ink-3);margin-top:8px">Durante la exploración del Libro Mayor se encontraron asientos contables sin contrapartida en ciertos meses — probablemente por cierres incompletos en el ERP. El skill Profit_Fiscal_Monitor los detecta y los marca como no confiables antes de cualquier conciliación.</p>
      </div>
    </div>
  </div>
</section>

<!-- ═══════════════════ CLAUDE.MD ═══════════════════ -->
<section>
  <div class="container">
    <p class="section-num">10 <span></span></p>
    <h2>El <em>CLAUDE.md</em> — manual del agente</h2>
    <p class="section-desc">El archivo central del proyecto define las reglas inviolables, la estructura de datos, y el comportamiento del agente. Es lo primero que Claude lee en cada sesión.</p>
    
    <div class="code-block">
      <div class="code-header"><span class="filename">CLAUDE.md (extracto)</span><span class="lang">Reglas inviolables</span></div>
      <div class="code-body"><span class="keyword">1.</span> <span class="string">MATCH PRIORITARIO:</span> Comparar Profit vs Excel. Diferencia = alerta.
<span class="keyword">2.</span> <span class="string">TODO EN MEMORIA:</span> NUNCA descargar archivos al disco local.
<span class="keyword">3.</span> <span class="string">SOLO LECTURA:</span> Nunca INSERT/UPDATE/DELETE contra Profit.
<span class="keyword">4.</span> <span class="string">AUDITORÍA:</span> Actualizar change_log.csv tras cada operación.
<span class="keyword">5.</span> <span class="string">VALIDACIÓN SYNC:</span> Verificar modifiedTime < 48h antes de procesar.
<span class="keyword">6.</span> <span class="string">SNAPSHOT:</span> Comparar KPIs vs corte anterior. Alerta si Δ > 20%.
<span class="keyword">7.</span> <span class="string">CONVERSIÓN:</span> Bs → USD con tasa BCV del día.</div>
    </div>
  </div>
</section>

<!-- ═══════════════════ DASHBOARD PREVIEW ═══════════════════ -->
<section>
  <div class="container">
    <p class="section-num">08 <span></span></p>
    <h2>El <em>dashboard</em></h2>
    <p class="section-desc">Un Live Artifact HTML de 80 KB con 7 vistas interactivas, filtros por empresa, búsqueda global, y datos detallados de las 5 empresas.</p>
    
    <div class="screenshot">
      <div class="bar">
        <span class="dot r"></span><span class="dot y"></span><span class="dot g"></span>
        <span class="url">claude.ai/cowork/nexara-dashboard-excel</span>
      </div>
      <div class="content">
        <div style="display:flex;gap:8px;margin-bottom:4px">
          <span style="padding:6px 14px;background:var(--surface-3);border-radius:4px;font-size:11px;color:var(--accent);font-weight:600;border-bottom:2px solid var(--accent)">Visión general</span>
          <span style="padding:6px 14px;font-size:11px;color:var(--ink-4)">Disponibilidad</span>
          <span style="padding:6px 14px;font-size:11px;color:var(--ink-4)">Ventas</span>
          <span style="padding:6px 14px;font-size:11px;color:var(--ink-4)">Inventario</span>
          <span style="padding:6px 14px;font-size:11px;color:var(--ink-4)">CxC</span>
          <span style="padding:6px 14px;font-size:11px;color:var(--ink-4)">CxP</span>
          <span style="padding:6px 14px;font-size:11px;color:var(--ink-4)">Buscar</span>
        </div>
        <div class="ss-kpis">
          <div class="ss-kpi"><div class="lbl">Resultado</div><div class="val" style="color:var(--green)">$8.1M</div></div>
          <div class="ss-kpi"><div class="lbl">Bancos</div><div class="val">$1.3M</div></div>
          <div class="ss-kpi"><div class="lbl">Ventas</div><div class="val">$11.2M</div></div>
          <div class="ss-kpi"><div class="lbl">Inventario</div><div class="val">$11.2M</div></div>
          <div class="ss-kpi"><div class="lbl">Por pagar</div><div class="val" style="color:var(--red)">-$19.4M</div></div>
        </div>
        <div class="ss-chart">
          <div class="ss-bar" style="height:180px;background:linear-gradient(to top, #1a9a8a, #2ab09a)"></div>
          <div class="ss-bar" style="height:80px;background:linear-gradient(to top, #6090c8, #7aa8d8)"></div>
          <div class="ss-bar" style="height:220px;background:linear-gradient(to top, #9070c0, #a888d0)"></div>
          <div class="ss-bar" style="height:140px;background:linear-gradient(to top, #c84050, #d85868)"></div>
          <div class="ss-bar" style="height:160px;background:linear-gradient(to top, #a03040, #c04858)"></div>
          <div class="ss-bar" style="height:250px;background:linear-gradient(to top, #9070c0, #a888d0)"></div>
          <div class="ss-bar" style="height:40px;background:linear-gradient(to top, #9070c0, #a888d0)"></div>
          <div class="ss-bar" style="height:200px;background:linear-gradient(to top, #a03040, #c04858)"></div>
        </div>
      </div>
    </div>
    
    <div class="grid-2" style="margin-top:24px">
      <div class="card">
        <h3>7 vistas interactivas</h3>
        <p style="font-size:14px;color:var(--ink-3);margin-top:8px">Visión general (KPIs + gráficos), Disponibilidad bancaria, Ventas (por año/mes/producto), Inventario (filtrable), Cuentas por cobrar, Cuentas por pagar, y Búsqueda global de partidas.</p>
      </div>
      <div class="card">
        <h3>Funcionalidades</h3>
        <p style="font-size:14px;color:var(--ink-3);margin-top:8px">Filtro global por empresa, búsqueda en cada tabla, filtro por categoría de producto, filtro por monto mínimo, drill-down expandible con +N partidas, dark mode automático.</p>
      </div>
    </div>
  </div>
</section>


<!-- ═══════════════════ FOOTER ═══════════════════ -->
<footer>
  <div class="container">
    <div class="left">Orquestación de datos · <em>Holding Nexara</em></div>
    <div class="right">Ing Jhonatan Mendoza - 2026</div>
  </div>
</footer>

</body>
</html>
