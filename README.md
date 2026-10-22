<!doctype html>
<html lang="ar" dir="rtl" data-theme="dark" data-font-size="md">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1,viewport-fit=cover">
<meta name="theme-color" content="#10b981">
<meta name="description" content="NexSec AI — Your Cybersecurity Development Workspace. Frontend-first, offline, honest about disabled integrations.">
<meta name="application-name" content="NexSec AI">
<title>NexSec AI — مساحة عمل تطوير الأمن السيبراني</title>
<link rel="icon" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 64 64'%3E%3Crect width='64' height='64' rx='14' fill='%230a0e12'/%3E%3Cpath d='M32 8 L52 16 L52 32 C52 44 42 54 32 58 C22 54 12 44 12 32 L12 16 Z' fill='none' stroke='%2310b981' stroke-width='3'/%3E%3Ccircle cx='32' cy='31' r='4' fill='%2334d399'/%3E%3C/svg%3E">
<style>
/* ═══════════════════════════════════════════════════════════════
   NEXSEC AI — STYLESHEET
   ═══════════════════════════════════════════════════════════════ */

/* ─────────── RESET ─────────── */
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
html{-webkit-text-size-adjust:100%;text-size-adjust:100%;scroll-behavior:smooth}
body{min-height:100vh;line-height:1.55;-webkit-font-smoothing:antialiased;-moz-osx-font-smoothing:grayscale}
img,svg,video,canvas{display:block;max-width:100%}
button,input,select,textarea{font:inherit;color:inherit}
button{background:none;border:none;cursor:pointer;padding:0;color:inherit}
a{color:inherit;text-decoration:none}
ul,ol{list-style:none}
table{border-collapse:collapse;border-spacing:0}
:focus-visible{outline:2px solid var(--accent);outline-offset:2px;border-radius:4px}
::selection{background:var(--accent-soft);color:var(--accent)}
@media (prefers-reduced-motion:reduce){
  *,*::before,*::after{animation-duration:.01ms!important;animation-iteration-count:1!important;transition-duration:.01ms!important;scroll-behavior:auto!important}
}

/* ─────────── DESIGN TOKENS ─────────── */
:root{
  /* Surfaces */
  --bg:#0a0e12;
  --bg-1:#0e1319;
  --bg-panel:#121820;
  --bg-elev:#1a222c;
  --bg-hover:#1f2a36;
  --bg-input:#0f141b;
  --bg-code:#070b0f;

  /* Borders */
  --border:#232c38;
  --border-2:#2e3947;
  --border-focus:#10b981;

  /* Text */
  --text:#e6edf3;
  --text-2:#8b97a5;
  --text-3:#5c6875;
  --text-4:#3a4452;

  /* Brand */
  --accent:#10b981;
  --accent-hi:#34d399;
  --accent-lo:#059669;
  --accent-soft:rgba(16,185,129,.12);
  --accent-glow:rgba(16,185,129,.35);

  /* Semantic */
  --success:#10b981;
  --warning:#f59e0b;
  --error:#ef4444;
  --info:#3b82f6;
  --success-soft:rgba(16,185,129,.12);
  --warning-soft:rgba(245,158,11,.12);
  --error-soft:rgba(239,68,68,.12);
  --info-soft:rgba(59,130,246,.12);

  /* Severity */
  --sev-info:#3b82f6;
  --sev-low:#10b981;
  --sev-med:#f59e0b;
  --sev-high:#f97316;
  --sev-crit:#ef4444;

  /* Radii */
  --r-xs:4px;
  --r-sm:6px;
  --r-md:10px;
  --r-lg:14px;
  --r-xl:20px;
  --r-full:999px;

  /* Spacing */
  --s-1:4px;
  --s-2:8px;
  --s-3:12px;
  --s-4:16px;
  --s-5:20px;
  --s-6:24px;
  --s-7:28px;
  --s-8:32px;
  --s-10:40px;
  --s-12:48px;

  /* Layout */
  --header-h:58px;
  --sidebar-w:250px;
  --sidebar-w-min:64px;
  --content-max:1320px;

  /* Typography */
  --font-sans:-apple-system,BlinkMacSystemFont,"Segoe UI","Noto Sans Arabic","Noto Sans",Roboto,"Helvetica Neue",Arial,sans-serif;
  --font-mono:"SF Mono","Cascadia Code","JetBrains Mono","Fira Code",Consolas,"Courier New",monospace;
  --fs-xs:.75rem;
  --fs-sm:.8125rem;
  --fs-md:.9375rem;
  --fs-lg:1.0625rem;
  --fs-xl:1.3125rem;
  --fs-2xl:1.75rem;
  --fs-3xl:2.25rem;

  /* Motion */
  --t-fast:100ms ease;
  --t-base:160ms ease;
  --t-slow:240ms cubic-bezier(.2,.6,.3,1);

  /* Shadows */
  --sh-sm:0 1px 2px rgba(0,0,0,.4);
  --sh-md:0 4px 16px rgba(0,0,0,.4);
  --sh-lg:0 12px 32px rgba(0,0,0,.5);
  --sh-focus:0 0 0 3px var(--accent-glow);
}

/* Font size scaling */
html[data-font-size="sm"]{--fs-md:.875rem;--fs-lg:1rem;--fs-xl:1.1875rem;--fs-2xl:1.5rem}
html[data-font-size="lg"]{--fs-md:1.0625rem;--fs-lg:1.1875rem;--fs-xl:1.5rem;--fs-2xl:2rem}

/* Light theme */
html[data-theme="light"]{
  --bg:#f5f7fa;
  --bg-1:#eef2f6;
  --bg-panel:#ffffff;
  --bg-elev:#f8fafc;
  --bg-hover:#eef2f6;
  --bg-input:#ffffff;
  --bg-code:#f8fafc;
  --border:#d8dee6;
  --border-2:#c3ccd6;
  --text:#0f172a;
  --text-2:#475569;
  --text-3:#94a3b8;
  --text-4:#cbd5e1;
}

/* ─────────── BASE ─────────── */
body{
  font-family:var(--font-sans);
  font-size:var(--fs-md);
  background:var(--bg);
  color:var(--text);
  display:grid;
  grid-template-areas:"header header" "sidebar main";
  grid-template-columns:var(--sidebar-w) 1fr;
  grid-template-rows:var(--header-h) 1fr;
  min-height:100vh;
  overflow-x:hidden;
}
body[data-sidebar="collapsed"]{grid-template-columns:var(--sidebar-w-min) 1fr}

/* ─────────── HEADER ─────────── */
.app-header{
  grid-area:header;
  position:sticky;top:0;z-index:40;
  display:flex;align-items:center;gap:var(--s-3);
  padding:0 var(--s-4);
  background:color-mix(in srgb,var(--bg-panel) 92%,transparent);
  backdrop-filter:blur(12px);-webkit-backdrop-filter:blur(12px);
  border-bottom:1px solid var(--border);
  height:var(--header-h);
}
.brand{display:flex;align-items:center;gap:var(--s-2);font-weight:600;font-size:var(--fs-md);letter-spacing:-.01em;transition:opacity var(--t-fast)}
.brand:hover{opacity:.85}
.brand__logo{width:30px;height:30px;flex-shrink:0}
.brand__name{background:linear-gradient(135deg,var(--text) 30%,var(--accent));-webkit-background-clip:text;background-clip:text;-webkit-text-fill-color:transparent;font-weight:700}
.brand__ver{font-size:var(--fs-xs);color:var(--text-3);font-weight:400;padding:2px 6px;border:1px solid var(--border);border-radius:var(--r-sm);margin-inline-start:4px}
.spacer{flex:1}
.hdr-status{
  display:inline-flex;align-items:center;gap:6px;
  padding:4px 10px;font-size:var(--fs-xs);
  background:var(--bg-elev);border:1px solid var(--border);
  border-radius:var(--r-full);color:var(--text-2);
}
.hdr-status__dot{width:7px;height:7px;border-radius:50%;background:var(--text-3);flex-shrink:0}
.hdr-status__dot--on{background:var(--success);box-shadow:0 0 0 2px var(--success-soft)}
.hdr-status__dot--off{background:var(--error);box-shadow:0 0 0 2px var(--error-soft)}
.hdr-status__dot--wait{background:var(--warning);box-shadow:0 0 0 2px var(--warning-soft)}

/* ─────────── SIDEBAR ─────────── */
.app-sidebar{
  grid-area:sidebar;
  position:sticky;top:var(--header-h);
  height:calc(100vh - var(--header-h));
  background:var(--bg-panel);
  border-inline-end:1px solid var(--border);
  padding:var(--s-3) var(--s-2);
  overflow-y:auto;overflow-x:hidden;
  display:flex;flex-direction:column;gap:2px;
  scrollbar-width:thin;
}
.app-sidebar::-webkit-scrollbar{width:6px}
.app-sidebar::-webkit-scrollbar-thumb{background:var(--border-2);border-radius:var(--r-full)}
.app-sidebar::-webkit-scrollbar-track{background:transparent}
.nav-group{
  font-size:var(--fs-xs);
  color:var(--text-3);
  padding:var(--s-4) var(--s-3) var(--s-1);
  text-transform:uppercase;
  letter-spacing:.08em;
  font-weight:600;
  white-space:nowrap;
  overflow:hidden;
}
.nav-link{
  display:flex;align-items:center;gap:var(--s-3);
  padding:var(--s-2) var(--s-3);
  border-radius:var(--r-md);
  color:var(--text-2);
  font-size:var(--fs-sm);
  font-weight:500;
  transition:background var(--t-fast),color var(--t-fast);
  position:relative;
  min-height:38px;
  white-space:nowrap;
}
.nav-link:hover{background:var(--bg-hover);color:var(--text)}
.nav-link[aria-current="page"]{
  background:var(--accent-soft);color:var(--accent);
}
.nav-link[aria-current="page"]::before{
  content:"";position:absolute;
  inset-inline-start:0;top:50%;transform:translateY(-50%);
  width:3px;height:20px;background:var(--accent);border-radius:var(--r-full);
}
.nav-link svg{width:18px;height:18px;flex-shrink:0}
.nav-link__badge{margin-inline-start:auto;font-size:var(--fs-xs);background:var(--bg-elev);padding:1px 6px;border-radius:var(--r-full);color:var(--text-3)}
body[data-sidebar="collapsed"] .app-sidebar .lbl,
body[data-sidebar="collapsed"] .app-sidebar .nav-group,
body[data-sidebar="collapsed"] .app-sidebar .nav-link__badge{display:none}
body[data-sidebar="collapsed"] .nav-link{justify-content:center;padding:var(--s-2)}

/* ─────────── MAIN ─────────── */
.app-main{
  grid-area:main;
  padding:var(--s-5) var(--s-6);
  overflow-x:hidden;
  min-width:0;
}
.page{
  max-width:var(--content-max);
  margin:0 auto;
  display:flex;flex-direction:column;gap:var(--s-5);
  animation:fadeIn .25s ease;
}
@keyframes fadeIn{from{opacity:0;transform:translateY(4px)}to{opacity:1;transform:none}}
.page-hdr{display:flex;flex-wrap:wrap;gap:var(--s-3);align-items:flex-start;justify-content:space-between}
.page-hdr__main{display:flex;flex-direction:column;gap:var(--s-1)}
.page-title{font-size:var(--fs-2xl);font-weight:700;letter-spacing:-.02em;line-height:1.2}
.page-sub{color:var(--text-2);font-size:var(--fs-sm)}

/* ─────────── LAYOUT HELPERS ─────────── */
.stack{display:flex;flex-direction:column;gap:var(--s-3)}
.stack-sm{gap:var(--s-2)}
.stack-lg{gap:var(--s-5)}
.stack-xl{gap:var(--s-6)}
.row{display:flex;gap:var(--s-2);align-items:center;flex-wrap:wrap}
.row-nowrap{flex-wrap:nowrap}
.row-between{justify-content:space-between}
.row-end{justify-content:flex-end}
.grid{display:grid;gap:var(--s-4)}
.grid-2{grid-template-columns:repeat(auto-fit,minmax(280px,1fr))}
.grid-3{grid-template-columns:repeat(auto-fit,minmax(220px,1fr))}
.grid-4{grid-template-columns:repeat(auto-fit,minmax(160px,1fr))}
.split{display:grid;grid-template-columns:1fr 1fr;gap:var(--s-4)}

/* ─────────── BUTTONS ─────────── */
.btn{
  display:inline-flex;align-items:center;justify-content:center;gap:var(--s-2);
  min-height:36px;padding:0 var(--s-4);
  border:1px solid var(--border-2);
  background:var(--bg-elev);
  color:var(--text);
  border-radius:var(--r-md);
  font-size:var(--fs-sm);font-weight:500;
  cursor:pointer;
  transition:background var(--t-fast),border-color var(--t-fast),color var(--t-fast),box-shadow var(--t-fast);
  white-space:nowrap;
  user-select:none;
}
.btn:hover{background:var(--bg-hover);border-color:var(--accent);color:var(--text)}
.btn:active{transform:translateY(1px)}
.btn:disabled{opacity:.5;cursor:not-allowed;background:var(--bg-elev);border-color:var(--border)}
.btn:disabled:hover{background:var(--bg-elev);border-color:var(--border)}
.btn svg{width:16px;height:16px;flex-shrink:0}
.btn-primary{background:var(--accent);border-color:var(--accent);color:#07110c;font-weight:600}
.btn-primary:hover{background:var(--accent-hi);border-color:var(--accent-hi);color:#07110c;box-shadow:0 0 0 3px var(--accent-glow)}
.btn-ghost{background:transparent;border-color:transparent;color:var(--text-2)}
.btn-ghost:hover{background:var(--bg-hover);color:var(--text)}
.btn-danger{background:var(--error-soft);border-color:var(--error);color:#fecaca}
.btn-danger:hover{background:var(--error);color:#fff;border-color:var(--error)}
.btn-sm{min-height:28px;padding:0 var(--s-3);font-size:var(--fs-xs)}
.btn-sm svg{width:14px;height:14px}
.btn-lg{min-height:44px;padding:0 var(--s-5);font-size:var(--fs-md)}
.btn-icon{padding:0;width:36px}
.btn-icon.btn-sm{width:28px}
.btn-group{display:inline-flex;border-radius:var(--r-md);overflow:hidden;border:1px solid var(--border-2)}
.btn-group .btn{border-radius:0;border:none;border-inline-end:1px solid var(--border-2)}
.btn-group .btn:last-child{border-inline-end:none}

/* ─────────── FORM INPUTS ─────────── */
.field{display:flex;flex-direction:column;gap:var(--s-1);min-width:0}
.field__lbl{font-size:var(--fs-xs);color:var(--text-2);font-weight:500;display:flex;align-items:center;gap:var(--s-1)}
.field__req{color:var(--error);font-size:var(--fs-xs)}
.field__hint{font-size:var(--fs-xs);color:var(--text-3)}
.input,.select,.textarea{
  width:100%;min-height:36px;
  padding:var(--s-2) var(--s-3);
  background:var(--bg-input);
  border:1px solid var(--border-2);
  border-radius:var(--r-md);
  color:var(--text);
  font-size:var(--fs-sm);
  transition:border-color var(--t-fast),box-shadow var(--t-fast);
}
.input:focus,.select:focus,.textarea:focus{
  border-color:var(--accent);outline:none;box-shadow:0 0 0 3px var(--accent-glow);
}
.input::placeholder,.textarea::placeholder{color:var(--text-3)}
.input:disabled,.textarea:disabled{opacity:.6;cursor:not-allowed}
.textarea{min-height:80px;resize:vertical;font-family:var(--font-sans);line-height:1.6}
.select{
  appearance:none;-webkit-appearance:none;
  background-image:url("data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='12' height='12' viewBox='0 0 24 24' fill='none' stroke='%238b97a5' stroke-width='2'><polyline points='6 9 12 15 18 9'/></svg>");
  background-repeat:no-repeat;background-position:right var(--s-3) center;
  padding-inline-end:var(--s-6);
}
html[dir="rtl"] .select{background-position:left var(--s-3) center}
.input-error{border-color:var(--error)}
.err{color:var(--error);font-size:var(--fs-xs)}
.search-wrap{position:relative}
.search-wrap .input{padding-inline-start:36px}
.search-wrap__icon{position:absolute;inset-inline-start:12px;top:50%;transform:translateY(-50%);width:16px;height:16px;color:var(--text-3);pointer-events:none}
.checkbox{display:flex;align-items:center;gap:var(--s-2);cursor:pointer;font-size:var(--fs-sm)}
.checkbox input{width:16px;height:16px;accent-color:var(--accent);cursor:pointer}

/* ─────────── CARDS ─────────── */
.card{
  background:var(--bg-panel);
  border:1px solid var(--border);
  border-radius:var(--r-lg);
  padding:var(--s-4);
  display:flex;flex-direction:column;gap:var(--s-3);
  transition:border-color var(--t-fast);
  position:relative;
}
.card-title{font-size:var(--fs-lg);font-weight:600;letter-spacing:-.01em;display:flex;align-items:center;gap:var(--s-2)}
.card-sub{font-size:var(--fs-xs);color:var(--text-2);line-height:1.5}
.card-hdr{display:flex;align-items:flex-start;justify-content:space-between;gap:var(--s-3);flex-wrap:wrap}
.card-body{font-size:var(--fs-sm);color:var(--text-2);line-height:1.6}
.card-footer{padding-top:var(--s-3);border-top:1px solid var(--border);display:flex;gap:var(--s-2);align-items:center;flex-wrap:wrap;margin-top:auto}
.card-inter{cursor:pointer}
.card-inter:hover{border-color:var(--accent);background:var(--bg-1)}
.card-inter:focus-within{border-color:var(--accent)}
.card-link{color:var(--accent);font-weight:500;transition:color var(--t-fast)}
.card-link:hover{color:var(--accent-hi);text-decoration:underline}

/* Stat cards */
.stat{display:flex;flex-direction:column;gap:var(--s-1)}
.stat__val{font-size:var(--fs-2xl);font-weight:700;color:var(--accent);line-height:1;letter-spacing:-.02em;font-variant-numeric:tabular-nums}
.stat__lbl{font-size:var(--fs-xs);color:var(--text-2);font-weight:500}
.stat__delta{font-size:var(--fs-xs);color:var(--text-3);display:flex;align-items:center;gap:4px}
.stat-card{position:relative;overflow:hidden;cursor:pointer}
.stat-card::after{
  content:"";position:absolute;inset-inline-end:-30px;inset-block-end:-30px;
  width:80px;height:80px;border-radius:50%;
  background:radial-gradient(circle,var(--accent-soft),transparent 70%);
  pointer-events:none;
}
.stat-card:hover{border-color:var(--accent)}

/* ─────────── BADGES / CHIPS ─────────── */
.badge{
  display:inline-flex;align-items:center;gap:5px;
  padding:2px 8px;font-size:var(--fs-xs);font-weight:500;
  border-radius:var(--r-full);
  border:1px solid var(--border-2);
  background:var(--bg-elev);
  color:var(--text-2);white-space:nowrap;
}
.badge svg{width:12px;height:12px}
.badge-ok{border-color:var(--success);color:var(--success);background:var(--success-soft)}
.badge-warn{border-color:var(--warning);color:var(--warning);background:var(--warning-soft)}
.badge-err{border-color:var(--error);color:#fca5a5;background:var(--error-soft)}
.badge-info{border-color:var(--info);color:#93c5fd;background:var(--info-soft)}
.badge-neutral{border-color:var(--border-2);color:var(--text-3)}
.chip{
  display:inline-flex;align-items:center;gap:5px;
  padding:3px 10px;font-size:var(--fs-xs);
  border-radius:var(--r-full);
  background:var(--bg-elev);border:1px solid var(--border-2);
  color:var(--text-2);
  cursor:pointer;transition:border-color var(--t-fast),color var(--t-fast);
}
.chip:hover{border-color:var(--accent);color:var(--accent)}
.chip-active{border-color:var(--accent);color:var(--accent);background:var(--accent-soft)}
.sev{display:inline-flex;align-items:center;gap:5px;padding:2px 8px;font-size:var(--fs-xs);border-radius:var(--r-full);font-weight:600;text-transform:uppercase;letter-spacing:.03em}
.sev-info{background:var(--info-soft);color:var(--info);border:1px solid var(--info)}
.sev-low{background:var(--success-soft);color:var(--success);border:1px solid var(--success)}
.sev-med{background:var(--warning-soft);color:var(--warning);border:1px solid var(--warning)}
.sev-high{background:rgba(249,115,22,.15);color:#f97316;border:1px solid #f97316}
.sev-crit{background:var(--error-soft);color:var(--error);border:1px solid var(--error)}

/* ─────────── EMPTY / BANNERS ─────────── */
.empty{
  display:flex;flex-direction:column;align-items:center;text-align:center;gap:var(--s-3);
  padding:var(--s-10) var(--s-5);
  color:var(--text-2);
  border:1px dashed var(--border-2);
  border-radius:var(--r-lg);
  background:var(--bg-1);
}
.empty__icon{width:48px;height:48px;opacity:.4;color:var(--text-3)}
.empty__title{color:var(--text);font-weight:600;font-size:var(--fs-md)}
.empty__desc{font-size:var(--fs-sm);max-width:400px;line-height:1.6}
.banner{
  display:flex;gap:var(--s-3);align-items:flex-start;
  padding:var(--s-3) var(--s-4);
  border-radius:var(--r-md);
  border:1px solid var(--border-2);
  background:var(--bg-elev);
  font-size:var(--fs-sm);
  line-height:1.5;
}
.banner svg{width:18px;height:18px;flex-shrink:0;margin-top:2px}
.banner-warn{border-color:var(--warning);background:var(--warning-soft);color:#fde68a}
.banner-warn svg{color:var(--warning)}
.banner-err{border-color:var(--error);background:var(--error-soft);color:#fecaca}
.banner-err svg{color:var(--error)}
.banner-info{border-color:var(--info);background:var(--info-soft);color:#bfdbfe}
.banner-info svg{color:var(--info)}
.banner-ok{border-color:var(--success);background:var(--success-soft);color:#a7f3d0}
.banner-ok svg{color:var(--success)}

/* ─────────── TOASTS ─────────── */
.toast-wrap{
  position:fixed;inset-block-start:calc(var(--header-h) + var(--s-3));inset-inline-end:var(--s-4);
  display:flex;flex-direction:column;gap:var(--s-2);
  z-index:100;max-width:min(380px,calc(100vw - 24px));
  pointer-events:none;
}
.toast{
  pointer-events:auto;display:flex;align-items:flex-start;gap:var(--s-2);
  padding:var(--s-3) var(--s-4);
  border-radius:var(--r-md);
  background:var(--bg-elev);
  border:1px solid var(--border-2);
  color:var(--text);
  font-size:var(--fs-sm);line-height:1.5;
  box-shadow:var(--sh-md);
  animation:toastIn var(--t-slow);
  position:relative;
}
.toast svg{width:18px;height:18px;flex-shrink:0;margin-top:1px}
.toast-ok{border-color:var(--success);background:var(--success-soft);color:#a7f3d0}
.toast-ok svg{color:var(--success)}
.toast-warn{border-color:var(--warning);background:var(--warning-soft);color:#fde68a}
.toast-warn svg{color:var(--warning)}
.toast-err{border-color:var(--error);background:var(--error-soft);color:#fecaca}
.toast-err svg{color:var(--error)}
.toast-info{border-color:var(--info);background:var(--info-soft);color:#bfdbfe}
.toast-info svg{color:var(--info)}
.toast__close{margin-inline-start:auto;color:inherit;opacity:.7;padding:0 4px;font-size:16px;line-height:1}
.toast__close:hover{opacity:1}
@keyframes toastIn{from{opacity:0;transform:translateX(20px)}to{opacity:1;transform:none}}
html[dir="rtl"] @keyframes toastIn{from{opacity:0;transform:translateX(-20px)}to{opacity:1;transform:none}}

/* ─────────── MODAL ─────────── */
.modal-back{
  position:fixed;inset:0;z-index:90;
  background:rgba(0,0,0,.72);
  backdrop-filter:blur(4px);-webkit-backdrop-filter:blur(4px);
  display:flex;align-items:center;justify-content:center;
  padding:var(--s-4);
  animation:fadeIn .15s ease;
}
.modal{
  width:100%;max-width:520px;
  background:var(--bg-panel);
  border:1px solid var(--border-2);
  border-radius:var(--r-lg);
  box-shadow:var(--sh-lg);
  padding:var(--s-5);
  display:flex;flex-direction:column;gap:var(--s-4);
  max-height:90vh;overflow-y:auto;
  animation:modalIn .2s cubic-bezier(.2,.6,.3,1);
}
@keyframes modalIn{from{opacity:0;transform:scale(.96) translateY(8px)}to{opacity:1;transform:none}}
.modal-title{font-size:var(--fs-lg);font-weight:600;letter-spacing:-.01em}
.modal-desc{color:var(--text-2);font-size:var(--fs-sm);line-height:1.6}
.modal-actions{display:flex;gap:var(--s-2);justify-content:flex-end;flex-wrap:wrap;margin-top:var(--s-1)}

/* ─────────── TABLES ─────────── */
.table-wrap{overflow-x:auto;border:1px solid var(--border);border-radius:var(--r-md);background:var(--bg-panel)}
.table{width:100%;font-size:var(--fs-sm);min-width:600px}
.table th,.table td{padding:var(--s-2) var(--s-3);text-align:start;border-bottom:1px solid var(--border)}
.table th{background:var(--bg-elev);color:var(--text-2);font-weight:600;font-size:var(--fs-xs);text-transform:uppercase;letter-spacing:.03em;position:sticky;top:0}
.table tbody tr:hover{background:var(--bg-1)}
.table tr:last-child td{border-bottom:none}

/* ─────────── CODE ─────────── */
.code-area{
  width:100%;min-height:340px;
  padding:var(--s-3);
  background:var(--bg-code);
  border:1px solid var(--border-2);
  border-radius:var(--r-md);
  color:var(--text);
  font-family:var(--font-mono);
  font-size:var(--fs-sm);line-height:1.6;
  direction:ltr;text-align:left;tab-size:2;
  resize:vertical;white-space:pre;overflow:auto;
  transition:border-color var(--t-fast);
}
.code-area:focus{outline:none;border-color:var(--accent);box-shadow:0 0 0 3px var(--accent-glow)}
.code-area::placeholder{color:var(--text-4)}
pre,code,.mono{font-family:var(--font-mono);direction:ltr;unicode-bidi:isolate;text-align:left}
pre{
  background:var(--bg-code);
  padding:var(--s-3);border-radius:var(--r-md);
  overflow-x:auto;font-size:var(--fs-xs);line-height:1.55;
  border:1px solid var(--border);
}
.code-block{position:relative}
.code-block__copy{position:absolute;inset-block-start:var(--s-2);inset-inline-end:var(--s-2);padding:4px 8px;font-size:var(--fs-xs);background:var(--bg-elev);border:1px solid var(--border);border-radius:var(--r-sm);color:var(--text-2);opacity:0;transition:opacity var(--t-fast)}
.code-block:hover .code-block__copy{opacity:1}
.code-block__copy:hover{color:var(--accent);border-color:var(--accent)}

/* ─────────── CHAT ─────────── */
.chat-layout{display:grid;grid-template-columns:240px 1fr;gap:var(--s-4);min-height:500px}
.chat-sidebar{display:flex;flex-direction:column;gap:var(--s-2)}
.chat-list{display:flex;flex-direction:column;gap:var(--s-1);max-height:62vh;overflow-y:auto;padding-inline-end:4px}
.chat-list::-webkit-scrollbar{width:6px}
.chat-list::-webkit-scrollbar-thumb{background:var(--border-2);border-radius:var(--r-full)}
.chat-item{
  display:flex;align-items:center;gap:var(--s-2);
  padding:var(--s-2) var(--s-3);
  border-radius:var(--r-md);
  cursor:pointer;font-size:var(--fs-sm);
  border:1px solid transparent;
  transition:background var(--t-fast);
  overflow:hidden;text-overflow:ellipsis;white-space:nowrap;
  min-height:38px;
}
.chat-item:hover{background:var(--bg-hover)}
.chat-item-active{background:var(--accent-soft);border-color:var(--accent);color:var(--accent)}
.chat-msgs{
  display:flex;flex-direction:column;gap:var(--s-3);
  padding:var(--s-4);
  background:var(--bg-input);
  border:1px solid var(--border);
  border-radius:var(--r-md);
  min-height:340px;max-height:56vh;overflow-y:auto;
  flex:1;
}
.chat-msgs::-webkit-scrollbar{width:6px}
.chat-msgs::-webkit-scrollbar-thumb{background:var(--border-2);border-radius:var(--r-full)}
.chat-msg{
  padding:var(--s-3) var(--s-4);
  border-radius:var(--r-md);
  background:var(--bg-elev);
  font-size:var(--fs-sm);line-height:1.6;
  word-wrap:break-word;overflow-wrap:break-word;
  max-width:100%;
}
.chat-msg-user{background:var(--accent-soft);border:1px solid var(--accent);margin-inline-start:auto;max-width:85%}
.chat-msg-system{background:var(--bg-panel);color:var(--text-2);border:1px dashed var(--border-2);text-align:center;font-size:var(--fs-xs);max-width:100%}
.chat-msg-meta{font-size:var(--fs-xs);color:var(--text-3);margin-top:var(--s-2);display:flex;gap:var(--s-2);align-items:center;flex-wrap:wrap}
.chat-msg-actions{display:flex;gap:var(--s-1);margin-inline-start:auto}
.chat-msg-btn{padding:2px 6px;font-size:var(--fs-xs);color:var(--text-3);border-radius:var(--r-sm);transition:color var(--t-fast),background var(--t-fast)}
.chat-msg-btn:hover{color:var(--accent);background:var(--bg-hover)}

/* ─────────── MISC ─────────── */
.flip{transform:scaleX(-1)}
.status{display:inline-flex;align-items:center;gap:6px;font-size:var(--fs-xs);color:var(--text-2);font-weight:500}
.status-dot{width:8px;height:8px;border-radius:50%;background:var(--text-3);flex-shrink:0}
.status-on{background:var(--success);box-shadow:0 0 0 3px var(--success-soft)}
.status-off{background:var(--error);box-shadow:0 0 0 3px var(--error-soft)}
.status-wait{background:var(--warning);box-shadow:0 0 0 3px var(--warning-soft)}
.hero{display:flex;gap:var(--s-5);align-items:center;flex-wrap:wrap;padding:var(--s-6);border:1px solid var(--border);background:linear-gradient(135deg,var(--bg-panel) 0%,var(--bg-elev) 100%);border-radius:var(--r-lg);position:relative;overflow:hidden}
.hero::before{content:"";position:absolute;inset-block-start:-100px;inset-inline-end:-100px;width:250px;height:250px;background:radial-gradient(circle,var(--accent-soft),transparent 60%);pointer-events:none}
.hero__logo{width:72px;height:72px;flex-shrink:0;position:relative;z-index:1}
.hero__body{flex:1;min-width:220px;position:relative;z-index:1}
.hero__title{font-size:var(--fs-xl);font-weight:700;letter-spacing:-.02em;margin-bottom:var(--s-1)}
.hero__sub{color:var(--text-2);font-size:var(--fs-sm)}
mark{background:var(--accent-soft);color:var(--accent);padding:0 2px;border-radius:2px;font-weight:500}
.danger-zone{border:1px solid var(--error);background:var(--error-soft);padding:var(--s-4);border-radius:var(--r-md);display:flex;flex-direction:column;gap:var(--s-3)}
.kv{display:flex;flex-direction:column;gap:2px}
.kv__k{font-size:var(--fs-xs);color:var(--text-3);text-transform:uppercase;letter-spacing:.04em;font-weight:500}
.kv__v{font-size:var(--fs-sm);color:var(--text)}
.kv-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(160px,1fr));gap:var(--s-4)}
.divider{height:1px;background:var(--border);border:none}
.toolbar{display:flex;gap:var(--s-2);align-items:center;flex-wrap:wrap;padding:var(--s-3);background:var(--bg-panel);border:1px solid var(--border);border-radius:var(--r-md)}
.toolbar .input,.toolbar .select{min-height:32px;font-size:var(--fs-sm)}
.list-item{display:flex;align-items:flex-start;gap:var(--s-3);padding:var(--s-3);border:1px solid var(--border);border-radius:var(--r-md);background:var(--bg-1);transition:border-color var(--t-fast)}
.list-item:hover{border-color:var(--border-2)}
.list-item__main{flex:1;min-width:0;display:flex;flex-direction:column;gap:var(--s-1)}
.list-item__title{font-weight:600;font-size:var(--fs-sm);display:flex;align-items:center;gap:var(--s-2);flex-wrap:wrap}
.list-item__sub{font-size:var(--fs-xs);color:var(--text-2);line-height:1.5}
.list-item__actions{display:flex;gap:var(--s-1);flex-wrap:wrap}
.tag-input{display:flex;flex-wrap:wrap;gap:var(--s-1);padding:var(--s-2);border:1px solid var(--border-2);border-radius:var(--r-md);background:var(--bg-input);min-height:36px}
.tag-input .chip{cursor:default}
.tag-input input{flex:1;min-width:80px;border:none;background:none;color:var(--text);font-size:var(--fs-sm);outline:none}
.steps{display:flex;flex-direction:column;gap:var(--s-2);counter-reset:step}
.steps__item{display:flex;gap:var(--s-3);align-items:flex-start;counter-increment:step}
.steps__item::before{content:counter(step);flex-shrink:0;width:24px;height:24px;border-radius:50%;background:var(--accent-soft);color:var(--accent);font-size:var(--fs-xs);font-weight:700;display:flex;align-items:center;justify-content:center;border:1px solid var(--accent)}
.steps__body{font-size:var(--fs-sm);line-height:1.6;flex:1}

/* ─────────── RESPONSIVE ─────────── */
@media (max-width:960px){
  body{grid-template-areas:"header" "main";grid-template-columns:1fr;grid-template-rows:var(--header-h) 1fr}
  .app-sidebar{
    position:fixed;inset-block:var(--header-h) 0;inset-inline-start:0;
    width:var(--sidebar-w);
    transform:translateX(-100%);
    transition:transform var(--t-slow);
    z-index:50;box-shadow:var(--sh-lg);
    border-inline-end:1px solid var(--border-2);
  }
  html[dir="rtl"] .app-sidebar{transform:translateX(100%)}
  body[data-drawer="open"] .app-sidebar{transform:none!important}
  body[data-drawer="open"]::after{content:"";position:fixed;inset:var(--header-h) 0 0 0;background:rgba(0,0,0,.55);z-index:45;animation:fadeIn .2s ease}
  .app-main{padding:var(--s-4)}
  .split{grid-template-columns:1fr}
  .chat-layout{grid-template-columns:1fr}
  .chat-list{max-height:160px}
}
@media (max-width:640px){
  :root{--header-h:54px}
  .app-header{padding:0 var(--s-3);gap:var(--s-2)}
  .brand__name,.brand__ver{display:none}
  .page-title{font-size:var(--fs-xl)}
  .page-sub{font-size:var(--fs-xs)}
  .app-main{padding:var(--s-3)}
  .card{padding:var(--s-3)}
  .modal{padding:var(--s-4);max-height:95vh}
  .hero{padding:var(--s-4);gap:var(--s-3)}
  .hero__logo{width:56px;height:56px}
  .hdr-status{padding:3px 8px;font-size:11px}
  .toast-wrap{inset-inline:var(--s-3);max-width:none}
  .btn{min-height:40px}
  .input,.select,.textarea{min-height:40px;font-size:16px}
  .grid-4{grid-template-columns:repeat(2,1fr)}
}
@media (max-width:400px){
  .grid-4{grid-template-columns:1fr}
  .btn-group{flex-direction:column}
  .btn-group .btn{border-inline-end:none;border-block-end:1px solid var(--border-2)}
  .btn-group .btn:last-child{border-block-end:none}
}
.hide-mobile{display:initial}
@media (max-width:720px){.hide-mobile{display:none!important}}
@media (min-width:721px){.hide-desktop{display:none!important}}

/* Print */
@media print{
  body{background:#fff;color:#000;display:block}
  .app-header,.app-sidebar,.toast-wrap,#modalRoot,.no-print,.btn,.page-actions{display:none!important}
  .app-main{padding:0}
  .card,.banner{border:1px solid #ccc;background:#fff;color:#000}
  .page{max-width:100%}
  a{color:#000;text-decoration:underline}
  pre{background:#f5f5f5;border:1px solid #ccc;color:#000}
}

/* Scrollbar (webkit) */
*::-webkit-scrollbar{width:8px;height:8px}
*::-webkit-scrollbar-thumb{background:var(--border-2);border-radius:var(--r-full)}
*::-webkit-scrollbar-thumb:hover{background:var(--text-4)}
*::-webkit-scrollbar-track{background:transparent}
</style>
</head>
<body data-sidebar="expanded" data-drawer="closed">

<!-- ═══════════════════════════════════════════════════════════════
     HEADER
     ═══════════════════════════════════════════════════════════════ -->
<header class="app-header" role="banner">
  <button id="menuToggle" class="btn btn-ghost btn-icon hide-desktop" aria-label="فتح القائمة" aria-expanded="false" aria-controls="appSidebar">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true">
      <line x1="3" y1="6" x2="21" y2="6"/><line x1="3" y1="12" x2="21" y2="12"/><line x1="3" y1="18" x2="21" y2="18"/>
    </svg>
  </button>

  <a href="#/dashboard" class="brand" aria-label="NexSec AI — الصفحة الرئيسية">
    <svg class="brand__logo" viewBox="0 0 64 64" aria-hidden="true">
      <rect width="64" height="64" rx="14" fill="#0a0e12"/>
      <path d="M32 8 L52 16 L52 32 C52 44 42 54 32 58 C22 54 12 44 12 32 L12 16 Z" fill="none" stroke="#10b981" stroke-width="2.5" stroke-linejoin="round"/>
      <polygon points="32,20 42,25.5 42,37 32,42.5 22,37 22,25.5" fill="none" stroke="#34d399" stroke-width="1.8" stroke-linejoin="round"/>
      <circle cx="32" cy="31.5" r="3" fill="#34d399"/>
    </svg>
    <span class="brand__name">NexSec AI</span>
    <span class="brand__ver" aria-label="version">v1.0</span>
  </a>

  <div class="spacer"></div>

  <span class="hdr-status hide-mobile" title="حالة الاتصال بمزوّد الذكاء الاصطناعي" role="status">
    <span class="hdr-status__dot hdr-status__dot--off" aria-hidden="true"></span>
    <span data-i18n="status.ai">AI: غير متصل</span>
  </span>

  <button id="langToggle" class="btn btn-ghost btn-sm" aria-label="تبديل اللغة" title="تبديل اللغة (AR / EN)">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true">
      <circle cx="12" cy="12" r="10"/><line x1="2" y1="12" x2="22" y2="12"/>
      <path d="M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"/>
    </svg>
    <span id="langLabel">EN</span>
  </button>

  <button id="sidebarToggle" class="btn btn-ghost btn-icon hide-mobile" aria-label="طي الشريط الجانبي" aria-controls="appSidebar" aria-expanded="true">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true">
      <polyline points="9 6 15 12 9 18" class="flip"/>
    </svg>
  </button>
</header>

<!-- ═══════════════════════════════════════════════════════════════
     SIDEBAR — التنقل الرئيسي
     ═══════════════════════════════════════════════════════════════ -->
<nav id="appSidebar" class="app-sidebar" role="navigation" aria-label="التنقل الرئيسي">

  <!-- ─── Workspace ─── -->
  <div class="nav-group" data-i18n="nav.workspace">مساحة العمل</div>

  <a href="#/dashboard" class="nav-link" data-route="dashboard">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true">
      <rect x="3" y="3" width="7" height="7" rx="1"/><rect x="14" y="3" width="7" height="7" rx="1"/>
      <rect x="14" y="14" width="7" height="7" rx="1"/><rect x="3" y="14" width="7" height="7" rx="1"/>
    </svg>
    <span class="lbl" data-i18n="nav.dashboard">لوحة التحكم</span>
  </a>

  <a href="#/chat" class="nav-link" data-route="chat">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true">
      <path d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z"/>
    </svg>
    <span class="lbl" data-i18n="nav.chat">المحادثة (تجريبي)</span>
  </a>

  <a href="#/code-studio" class="nav-link" data-route="code-studio">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true">
      <polyline points="16 18 22 12 16 6"/><polyline points="8 6 2 12 8 18"/>
    </svg>
    <span class="lbl" data-i18n="nav.codeStudio">استوديو الكود</span>
  </a>

  <a href="#/repositories" class="nav-link" data-route="repositories">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true">
      <circle cx="11" cy="11" r="8"/><line x1="21" y1="21" x2="16.65" y2="16.65"/>
    </svg>
    <span class="lbl" data-i18n="nav.repos">البحث في المستودعات</span>
  </a>

  <!-- ─── Library ─── -->
  <div class="nav-group" data-i18n="nav.library">المكتبة</div>

  <a href="#/scripts" class="nav-link" data-route="scripts">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true">
      <path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/>
      <polyline points="14 2 14 8 20 8"/><line x1="9" y1="15" x2="15" y2="15"/>
    </svg>
    <span class="lbl" data-i18n="nav.scripts">مكتبة السكربتات</span>
  </a>

  <a href="#/tools" class="nav-link" data-route="tools">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true">
      <path d="M14.7 6.3a4 4 0 1 0 5 5L21 12l-9 9-9-9 9-9z"/>
    </svg>
    <span class="lbl" data-i18n="nav.tools">أدوات الأمن</span>
  </a>

  <a href="#/knowledge" class="nav-link" data-route="knowledge">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true">
      <path d="M4 19.5A2.5 2.5 0 0 1 6.5 17H20"/>
      <path d="M6.5 2H20v20H6.5A2.5 2.5 0 0 1 4 19.5v-15A2.5 2.5 0 0 1 6.5 2z"/>
    </svg>
    <span class="lbl" data-i18n="nav.knowledge">قاعدة المعرفة</span>
  </a>

  <!-- ─── Manage ─── -->
  <div class="nav-group" data-i18n="nav.manage">الإدارة</div>

  <a href="#/projects" class="nav-link" data-route="projects">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true">
      <path d="M3 7a2 2 0 0 1 2-2h4l2 2h8a2 2 0 0 1 2 2v8a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"/>
    </svg>
    <span class="lbl" data-i18n="nav.projects">المشاريع</span>
  </a>

  <a href="#/reports" class="nav-link" data-route="reports">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true">
      <path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/>
      <polyline points="14 2 14 8 20 8"/>
      <line x1="8" y1="13" x2="16" y2="13"/><line x1="8" y1="17" x2="13" y2="17"/>
    </svg>
    <span class="lbl" data-i18n="nav.reports">التقارير الأمنية</span>
  </a>

  <!-- ─── System ─── -->
  <div class="nav-group" data-i18n="nav.system">النظام</div>

  <a href="#/settings" class="nav-link" data-route="settings">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true">
      <circle cx="12" cy="12" r="3"/>
      <path d="M19.4 15a1.65 1.65 0 0 0 .33 1.82l.06.06a2 2 0 1 1-2.83 2.83l-.06-.06a1.65 1.65 0 0 0-1.82-.33 1.65 1.65 0 0 0-1 1.51V21a2 2 0 1 1-4 0v-.09A1.65 1.65 0 0 0 9 19.4a1.65 1.65 0 0 0-1.82.33l-.06.06a2 2 0 1 1-2.83-2.83l.06-.06a1.65 1.65 0 0 0 .33-1.82 1.65 1.65 0 0 0-1.51-1H3a2 2 0 1 1 0-4h.09A1.65 1.65 0 0 0 4.6 9a1.65 1.65 0 0 0-.33-1.82l-.06-.06a2 2 0 1 1 2.83-2.83l.06.06a1.65 1.65 0 0 0 1.82.33H9a1.65 1.65 0 0 0 1-1.51V3a2 2 0 1 1 4 0v.09A1.65 1.65 0 0 0 15 4.6a1.65 1.65 0 0 0 1.82-.33l.06-.06a2 2 0 1 1 2.83 2.83l-.06.06a1.65 1.65 0 0 0-.33 1.82V9a1.65 1.65 0 0 0 1.51 1H21a2 2 0 1 1 0 4h-.09A1.65 1.65 0 0 0 19.4 15z"/>
    </svg>
    <span class="lbl" data-i18n="nav.settings">الإعدادات</span>
  </a>

  <a href="#/about" class="nav-link" data-route="about">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true">
      <circle cx="12" cy="12" r="10"/>
      <line x1="12" y1="16" x2="12" y2="12"/><line x1="12" y1="8" x2="12.01" y2="8"/>
    </svg>
    <span class="lbl" data-i18n="nav.about">حول التطبيق</span>
  </a>

  <div class="spacer"></div>

  <div class="hide-desktop" style="padding:var(--s-3) var(--s-2);font-size:var(--fs-xs);color:var(--text-3);border-top:1px solid var(--border);margin-top:var(--s-3)">
    <div style="font-weight:600;color:var(--text-2)">NexSec AI</div>
    <div data-i18n="app.version">الإصدار 1.0 — Frontend-First</div>
  </div>
</nav>

<!-- ═══════════════════════════════════════════════════════════════
     MAIN — حاوية الصفحات (Router يملأها)
     ═══════════════════════════════════════════════════════════════ -->
<main id="appMain" class="app-main" role="main" tabindex="-1">
  <div class="page">
    <div class="empty">
      <svg class="empty__icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" aria-hidden="true">
        <circle cx="12" cy="12" r="10"/><path d="M12 6v6l4 2"/>
      </svg>
      <div class="empty__title" data-i18n="common.loading">جارٍ التحميل…</div>
    </div>
  </div>
</main>

<!-- ═══════════════════════════════════════════════════════════════
     TOAST + MODAL ROOTS
     ═══════════════════════════════════════════════════════════════ -->
<div id="toastWrap" class="toast-wrap" role="status" aria-live="polite" aria-atomic="false"></div>
<div id="modalRoot"></div>

<!-- ═══════════════════════════════════════════════════════════════
     JAVASCRIPT
     ═══════════════════════════════════════════════════════════════ -->
<script>
'use strict';

/* ═══════════════════════════════════════════════════════════════
   1. UTILITIES — دوال مساعدة عامة (بدون أي اعتماديات)
   ═══════════════════════════════════════════════════════════════ */

const $ = (sel, root = document) => root.querySelector(sel);
const $$ = (sel, root = document) => Array.from(root.querySelectorAll(sel));

/**
 * إنشاء عنصر DOM برمجياً (آمن — لا يقبل HTML غير موثوق عبر `text`)
 */
function el(tag, attrs = {}, ...children) {
  const node = document.createElement(tag);
  for (const [key, val] of Object.entries(attrs)) {
    if (val == null || val === false) continue;
    if (key === 'class') node.className = val;
    else if (key === 'text') node.textContent = String(val);
    else if (key === 'html') node.innerHTML = String(val);
    else if (key === 'dataset') Object.assign(node.dataset, val);
    else if (key === 'style' && typeof val === 'object') Object.assign(node.style, val);
    else if (key.startsWith('on') && typeof val === 'function') {
      node.addEventListener(key.slice(2).toLowerCase(), val);
    } else {
      node.setAttribute(key, val === true ? '' : String(val));
    }
  }
  for (const child of children.flat(Infinity)) {
    if (child == null || child === false) continue;
    node.appendChild(typeof child === 'string' || typeof child === 'number'
      ? document.createTextNode(String(child))
      : child);
  }
  return node;
}

function escapeHtml(str) {
  return String(str ?? '')
    .replace(/&/g, '&amp;')
    .replace(/</g, '&lt;')
    .replace(/>/g, '&gt;')
    .replace(/"/g, '&quot;')
    .replace(/'/g, '&#39;');
}

function uid(prefix = '') {
  return prefix + Date.now().toString(36) + Math.random().toString(36).slice(2, 8);
}

function debounce(fn, wait = 250) {
  let t;
  const wrapped = (...args) => {
    clearTimeout(t);
    t = setTimeout(() => fn(...args), wait);
  };
  wrapped.cancel = () => clearTimeout(t);
  return wrapped;
}

function throttle(fn, wait = 200) {
  let last = 0, timer;
  return (...args) => {
    const now = Date.now();
    const remaining = wait - (now - last);
    if (remaining <= 0) {
      clearTimeout(timer);
      last = now;
      fn(...args);
    } else {
      clearTimeout(timer);
      timer = setTimeout(() => { last = Date.now(); fn(...args); }, remaining);
    }
  };
}

function download(filename, content, mime = 'text/plain;charset=utf-8') {
  try {
    const blob = content instanceof Blob ? content : new Blob([content], { type: mime });
    const url = URL.createObjectURL(blob);
    const a = document.createElement('a');
    a.href = url;
    a.download = sanitizeFilename(filename);
    document.body.appendChild(a);
    a.click();
    a.remove();
    setTimeout(() => URL.revokeObjectURL(url), 1500);
    return true;
  } catch (err) {
    console.error('Download failed:', err);
    return false;
  }
}

async function copyText(text) {
  try {
    if (navigator.clipboard?.writeText) {
      await navigator.clipboard.writeText(text);
      return true;
    }
  } catch {}
  try {
    const ta = document.createElement('textarea');
    ta.value = text;
    ta.setAttribute('readonly', '');
    ta.style.cssText = 'position:fixed;opacity:0;pointer-events:none';
    document.body.appendChild(ta);
    ta.select();
    const ok = document.execCommand('copy');
    ta.remove();
    return ok;
  } catch { return false; }
}

function sanitizeFilename(name) {
  const base = String(name || 'file')
    .replace(/[<>:"/\\|?*\x00-\x1f]/g, '_')
    .replace(/\s+/g, '_')
    .replace(/_+/g, '_')
    .replace(/^_|_$/g, '')
    .slice(0, 100) || 'file';
  return base;
}

function formatDate(ts, locale) {
  if (!ts) return '—';
  const lang = locale || i18n.current || 'ar';
  try {
    return new Intl.DateTimeFormat(lang === 'ar' ? 'ar-EG' : 'en-US', {
      year: 'numeric', month: 'short', day: 'numeric',
      hour: '2-digit', minute: '2-digit'
    }).format(new Date(ts));
  } catch {
    try { return new Date(ts).toISOString().slice(0, 16).replace('T', ' '); }
    catch { return String(ts); }
  }
}

function formatRelative(ts, locale) {
  if (!ts) return '—';
  const lang = locale || i18n.current || 'ar';
  const diff = (Date.now() - new Date(ts).getTime()) / 1000;
  if (diff < 60) return lang === 'ar' ? 'الآن' : 'just now';
  if (diff < 3600) {
    const m = Math.floor(diff / 60);
    return lang === 'ar' ? `قبل ${m} دقيقة` : `${m}m ago`;
  }
  if (diff < 86400) {
    const h = Math.floor(diff / 3600);
    return lang === 'ar' ? `قبل ${h} ساعة` : `${h}h ago`;
  }
  if (diff < 604800) {
    const d = Math.floor(diff / 86400);
    return lang === 'ar' ? `قبل ${d} يوم` : `${d}d ago`;
  }
  return formatDate(ts, lang);
}

function fileExtension(lang) {
  const map = {
    python: 'py', javascript: 'js', typescript: 'ts', html: 'html', css: 'css',
    bash: 'sh', shell: 'sh', powershell: 'ps1', c: 'c', cpp: 'cpp',
    go: 'go', rust: 'rs', sql: 'sql', json: 'json', yaml: 'yml',
    xml: 'xml', markdown: 'md', text: 'txt', other: 'txt'
  };
  return map[lang] || 'txt';
}

function highlightMatch(text, query) {
  const safe = escapeHtml(text);
  if (!query || !query.trim()) return safe;
  const q = query.trim();
  try {
    const pattern = q.replace(/[.*+?^${}()|[\]\\]/g, '\\$&');
    return safe.replace(new RegExp(`(${pattern})`, 'gi'), '<mark>$1</mark>');
  } catch { return safe; }
}

function clamp(n, min, max) { return Math.max(min, Math.min(max, n)); }
function sleep(ms) { return new Promise(r => setTimeout(r, ms)); }

function safeJSON(str, fallback = null) {
  try { return JSON.parse(str); }
  catch { return fallback; }
}

function truncate(str, max = 80) {
  const s = String(str ?? '');
  if (s.length <= max) return s;
  return s.slice(0, max - 1) + '…';
}

/* ═══════════════════════════════════════════════════════════════
   2. STORAGE — طبقة التخزين
   ═══════════════════════════════════════════════════════════════ */

const Storage = (() => {
  const PREFIX = 'nexsec.v1.';
  const SCHEMA_VERSION = 1;
  let available = true;
  const memory = {};

  try {
    const k = '__nexsec_test__';
    localStorage.setItem(k, '1');
    localStorage.removeItem(k);
  } catch { available = false; }

  function fullKey(k) { return PREFIX + k; }

  function rawGet(k) {
    if (available) {
      try { return localStorage.getItem(fullKey(k)); } catch {}
    }
    return Object.prototype.hasOwnProperty.call(memory, k) ? memory[k] : null;
  }

  function rawSet(k, v) {
    if (available) {
      try {
        localStorage.setItem(fullKey(k), v);
        return true;
      } catch (err) {
        if (err && (err.name === 'QuotaExceededError' || err.code === 22)) {
          console.warn('NexSec: تخزين ممتلئ — تم تجاهل الحفظ.');
          return false;
        }
      }
    }
    memory[k] = v;
    return false;
  }

  function rawRemove(k) {
    if (available) {
      try { localStorage.removeItem(fullKey(k)); } catch {}
    }
    delete memory[k];
  }

  function get(key, fallback = null) {
    const raw = rawGet(key);
    if (raw == null) return fallback;
    const parsed = safeJSON(raw, null);
    if (parsed && typeof parsed === 'object' && parsed.__v === SCHEMA_VERSION && 'data' in parsed) {
      return parsed.data;
    }
    return parsed != null ? parsed : fallback;
  }

  function set(key, value) {
    const envelope = { __v: SCHEMA_VERSION, data: value };
    return rawSet(key, JSON.stringify(envelope));
  }

  function remove(key) { rawRemove(key); }

  function keys() {
    const out = [];
    if (available) {
      try {
        for (let i = 0; i < localStorage.length; i++) {
          const k = localStorage.key(i);
          if (k && k.startsWith(PREFIX)) out.push(k.slice(PREFIX.length));
        }
      } catch {}
    }
    for (const k of Object.keys(memory)) out.push(k);
    return Array.from(new Set(out));
  }

  function clearAll() {
    for (const k of keys()) rawRemove(k);
  }

  function exportAll() {
    const dump = {
      _app: 'nexsec-ai',
      _schema: SCHEMA_VERSION,
      _exportedAt: new Date().toISOString(),
      _count: 0,
      data: {}
    };
    for (const key of keys()) dump.data[key] = get(key);
    dump._count = Object.keys(dump.data).length;
    return dump;
  }

  function importAll(dump, { merge = false } = {}) {
    if (!dump || typeof dump !== 'object' || dump._app !== 'nexsec-ai') {
      throw new Error('invalid_file');
    }
    if (!dump.data || typeof dump.data !== 'object') {
      throw new Error('invalid_file');
    }
    if (!merge) clearAll();
    let count = 0;
    for (const [key, value] of Object.entries(dump.data)) {
      set(key, value);
      count++;
    }
    return count;
  }

  return {
    available: () => available,
    get, set, remove, keys, clearAll,
    exportAll, importAll
  };
})();

/* ═══════════════════════════════════════════════════════════════
   3. I18N — نظام الترجمة (عربي / إنجليزي)
   ═══════════════════════════════════════════════════════════════ */

const I18N = {
  ar: {
    /* App */
    'app.name': 'NexSec AI',
    'app.tagline': 'مساحة عمل تطوير الأمن السيبراني',
    'app.version': 'الإصدار 1.0 — Frontend-First',

    /* Nav */
    'nav.workspace': 'مساحة العمل',
    'nav.library': 'المكتبة',
    'nav.manage': 'الإدارة',
    'nav.system': 'النظام',
    'nav.dashboard': 'لوحة التحكم',
    'nav.chat': 'المحادثة (تجريبي)',
    'nav.codeStudio': 'استوديو الكود',
    'nav.repos': 'البحث في المستودعات',
    'nav.scripts': 'مكتبة السكربتات',
    'nav.tools': 'أدوات الأمن',
    'nav.knowledge': 'قاعدة المعرفة',
    'nav.projects': 'المشاريع',
    'nav.reports': 'التقارير الأمنية',
    'nav.settings': 'الإعدادات',
    'nav.about': 'حول التطبيق',

    /* Status */
    'status.ai': 'AI: غير متصل',
    'status.repo': 'المستودعات: بدون اتصال',
    'status.backend': 'الخادم الخلفي: معطّل',
    'status.aiLong': 'مزوّد الذكاء الاصطناعي غير متصل بهذا الإصدار',
    'status.repoLong': 'البحث المباشر في المستودعات معطّل — يفتح بحث GitHub الرسمي',
    'status.backendLong': 'لا يوجد خادم خلفي متصل',

    /* Common */
    'common.save': 'حفظ',
    'common.cancel': 'إلغاء',
    'common.delete': 'حذف',
    'common.edit': 'تعديل',
    'common.close': 'إغلاق',
    'common.confirm': 'تأكيد',
    'common.search': 'بحث',
    'common.clear': 'مسح',
    'common.create': 'إنشاء',
    'common.copy': 'نسخ',
    'common.copied': 'تم النسخ',
    'common.download': 'تنزيل',
    'common.export': 'تصدير',
    'common.import': 'استيراد',
    'common.add': 'إضافة',
    'common.name': 'الاسم',
    'common.title': 'العنوان',
    'common.description': 'الوصف',
    'common.category': 'الفئة',
    'common.language': 'اللغة',
    'common.status': 'الحالة',
    'common.created': 'تاريخ الإنشاء',
    'common.updated': 'آخر تحديث',
    'common.actions': 'إجراءات',
    'common.none': 'لا يوجد',
    'common.loading': 'جارٍ التحميل…',
    'common.optional': 'اختياري',
    'common.required': 'مطلوب',
    'common.yes': 'نعم',
    'common.no': 'لا',
    'common.na': 'غير متاح',
    'common.back': 'رجوع',
    'common.next': 'التالي',
    'common.prev': 'السابق',
    'common.retry': 'إعادة المحاولة',
    'common.reset': 'إعادة تعيين',
    'common.refresh': 'تحديث',
    'common.view': 'عرض',
    'common.open': 'فتح',
    'common.apply': 'تطبيق',
    'common.filter': 'تصفية',
    'common.sort': 'ترتيب',
    'common.all': 'الكل',
    'common.on': 'مفعّل',
    'common.off': 'معطّل',
    'common.ok': 'حسناً',
    'common.error': 'خطأ',
    'common.warning': 'تحذير',
    'common.info': 'معلومة',
    'common.success': 'نجاح',
    'common.unknown': 'غير معروف',
    'common.other': 'أخرى',
    'common.tags': 'الوسوم',
    'common.notes': 'ملاحظات',
    'common.version': 'الإصدار',
    'common.menu': 'القائمة',
    'common.saved': 'تم الحفظ',
    'common.deleted': 'تم الحذف',
    'common.created_ok': 'تم الإنشاء',
    'common.updated_ok': 'تم التحديث',
    'common.unsaved': 'تغييرات غير محفوظة',
    'common.confirmDelete': 'تأكيد الحذف',
    'common.deleteWarning': 'لا يمكن التراجع عن هذا الإجراء.',
    'common.searchPlaceholder': 'ابحث…',
    'common.noResults': 'لا توجد نتائج',
    'common.viewAll': 'عرض الكل',
    'common.quickActions': 'إجراءات سريعة',

    /* Empty states */
    'empty.scripts': 'لا توجد سكربتات محفوظة بعد',
    'empty.scriptsDesc': 'استخدم استوديو الكود أو أنشئ سكربتاً جديداً هنا',
    'empty.projects': 'لا توجد مشاريع بعد',
    'empty.projectsDesc': 'أنشئ مشروعاً جديداً لتنظيم عملك',
    'empty.reports': 'لا توجد تقارير بعد',
    'empty.reportsDesc': 'أنشئ تقريراً أمنياً جديداً',
    'empty.chats': 'لا توجد محادثات بعد',
    'empty.chatsDesc': 'ابدأ محادثة جديدة',
    'empty.search': 'لا توجد نتائج لبحثك',
    'empty.searchDesc': 'جرّب كلمات أخرى أو أزل عوامل التصفية',
    'empty.generic': 'لا يوجد محتوى بعد',
    'empty.toolsNotes': 'لا توجد ملاحظات على هذه الأداة',

    /* Errors */
    'error.storageUnavailable': 'التخزين المحلي غير متاح — لن يتم حفظ البيانات',
    'error.storageQuota': 'مساحة التخزين ممتلئة — احذف بعض البيانات',
    'error.generic': 'حدث خطأ غير متوقع',
    'error.notFound': 'الصفحة غير موجودة',
    'error.notFoundDesc': 'تحقق من العنوان أو عد إلى لوحة التحكم',
    'error.invalidFile': 'ملف غير صالح — تأكد أنه تصدير NexSec AI',
    'error.required': 'هذا الحقل مطلوب',
    'error.tooShort': 'النص قصير جداً',
    'error.tooLong': 'النص طويل جداً',
    'error.aiUnavailable': 'الذكاء الاصطناعي غير متصل',
    'error.aiUnavailableDesc': 'هذه الميزة تتطلب ربط مزوّد AI — غير متاح في v1.0',
    'error.repoUnavailable': 'البحث المباشر معطّل',
    'error.repoUnavailableDesc': 'استخدم زر البحث في GitHub الرسمي',
    'error.analysisUnavailable': 'التحليل التلقائي غير متاح',
    'error.analysisUnavailableDesc': 'استخدم قائمة التحقق اليدوية',

    /* Severity */
    'sev.info': 'معلوماتي',
    'sev.low': 'منخفض',
    'sev.med': 'متوسط',
    'sev.high': 'عالي',
    'sev.crit': 'حرج',

    /* Settings */
    'settings.title': 'الإعدادات',
    'settings.language': 'اللغة',
    'settings.languageDesc': 'اختر لغة الواجهة',
    'settings.theme': 'السمة',
    'settings.themeDesc': 'داكن أو فاتح',
    'settings.themeDark': 'داكن',
    'settings.themeLight': 'فاتح',
    'settings.fontSize': 'حجم الخط',
    'settings.fontSizeDesc': 'صغير / متوسط / كبير',
    'settings.fontSm': 'صغير',
    'settings.fontMd': 'متوسط',
    'settings.fontLg': 'كبير',
    'settings.reduceMotion': 'تقليل الحركة',
    'settings.reduceMotionDesc': 'تعطيل الرسوم المتحركة',
    'settings.status': 'حالة الاتصالات',
    'settings.privacy': 'الخصوصية',
    'settings.privacyDesc': 'كل البيانات محفوظة محلياً في متصفحك فقط. لا يتم إرسال أي معلومات إلى أي خادم.',
    'settings.reset': 'إعادة تعيين الإعدادات',
    'settings.resetConfirm': 'هل تريد إعادة تعيين الإعدادات إلى القيم الافتراضية؟',
    'settings.clearData': 'حذف كل البيانات المحلية',
    'settings.clearDataConfirm': 'سيتم حذف كل المشاريع والسكربتات والتقارير والمحادثات. لا يمكن التراجع!',
    'settings.export': 'تصدير البيانات',
    'settings.exportDesc': 'تنزيل نسخة احتياطية JSON من كل بياناتك',
    'settings.import': 'استيراد البيانات',
    'settings.importDesc': 'استعادة نسخة احتياطية (سيستبدل البيانات الحالية)',
    'settings.about': 'حول التطبيق',

    /* Dashboard */
    'dashboard.title': 'لوحة التحكم',
    'dashboard.welcome': 'مرحباً بك في NexSec AI',
    'dashboard.subtitle': 'مساحة عمل تطوير الأمن السيبراني',
    'dashboard.projects': 'المشاريع',
    'dashboard.scripts': 'السكربتات',
    'dashboard.reports': 'التقارير',
    'dashboard.chats': 'المحادثات',
    'dashboard.recentProjects': 'أحدث المشاريع',
    'dashboard.recentScripts': 'أحدث السكربتات',
    'dashboard.recentReports': 'أحدث التقارير',
    'dashboard.quickStart': 'بدء سريع',
    'dashboard.noRecent': 'لا يوجد بعد',

    /* Chat */
    'chat.title': 'المحادثة',
    'chat.new': 'محادثة جديدة',
    'chat.rename': 'إعادة تسمية',
    'chat.delete': 'حذف المحادثة',
    'chat.clear': 'تفريغ المحادثة',
    'chat.placeholder': 'اكتب رسالتك… (Enter للإرسال، Shift+Enter لسطر جديد)',
    'chat.send': 'إرسال',
    'chat.aiNotConnected': 'الذكاء الاصطناعي غير متصل',
    'chat.aiNotConnectedDesc': 'هذا وضع تجريبي محلي. الرسائل تُحفظ فقط — لا يتم إرسالها لأي نموذج.',
    'chat.demoNotice': 'وضع عرض محلي — لن تحصل على ردود ذكاء اصطناعي في v1.0',
    'chat.empty': 'ابدأ محادثة جديدة من القائمة',
    'chat.noConversation': 'لم تُختر محادثة',
    'chat.message': 'رسالة',
    'chat.messages': 'رسائل',

    /* Code Studio */
    'code.title': 'استوديو الكود',
    'code.subtitle': 'تحرير وحفظ السكربتات بأمان',
    'code.editor': 'المحرر',
    'code.titleField': 'عنوان الكود',
    'code.descField': 'وصف قصير',
    'code.langField': 'لغة البرمجة',
    'code.lineCount': 'الأسطر',
    'code.charCount': 'الأحرف',
    'code.save': 'حفظ في المكتبة',
    'code.saveDraft': 'حفظ كمسودة',
    'code.clear': 'مسح المحرر',
    'code.clearConfirm': 'هل تريد مسح المحرر؟ سيتم فقدان التغييرات غير المحفوظة.',
    'code.explain': 'شرح الكود',
    'code.explainUnavailable': 'الشرح غير متاح حتى يتم ربط الذكاء الاصطناعي',
    'code.review': 'مراجعة الكود',
    'code.reviewManual': 'استخدم قائمة التحقق اليدوية أدناه',
    'code.find': 'بحث في الكود',
    'code.findPlaceholder': 'ابحث عن نص…',
    'code.noMatch': 'لا تطابق',
    'code.attachToProject': 'ربط بمشروع',

    /* Scripts */
    'scripts.title': 'مكتبة السكربتات',
    'scripts.new': 'سكربت جديد',
    'scripts.filterLang': 'تصفية باللغة',
    'scripts.filterCat': 'تصفية بالفئة',
    'scripts.sortBy': 'ترتيب حسب',
    'scripts.sortCreated': 'تاريخ الإنشاء',
    'scripts.sortUpdated': 'آخر تحديث',
    'scripts.favorite': 'مفضّل',
    'scripts.unfavorite': 'إزالة من المفضلة',
    'scripts.warn': 'تحذير: السكربتات المستوردة غير موثوقة. لا تشغّلها دون مراجعة.',

    /* Tools */
    'tools.title': 'أدوات الأمن',
    'tools.subtitle': 'مرجع تعليمي لأدوات الأمن السيبراني',
    'tools.docs': 'التوثيق الرسمي',
    'tools.category': 'الفئة',
    'tools.platform': 'المنصات',
    'tools.license': 'الترخيص',
    'tools.notes': 'ملاحظاتي',
    'tools.bookmark': 'حفظ',
    'tools.unbookmark': 'إزالة الحفظ',
    'tools.disclaimer': 'هذه المعلومات مرجعية تعليمية فقط. لم يتم التحقق من تثبيت أو تشغيل أي أداة.',

    /* Knowledge */
    'knowledge.title': 'قاعدة المعرفة',
    'knowledge.subtitle': 'مقالات ومراجع تعليمية',
    'knowledge.categories': 'الفئات',
    'knowledge.article': 'مقال',
    'knowledge.readMore': 'اقرأ المزيد',
    'knowledge.bookmark': 'حفظ',
    'knowledge.unbookmark': 'إزالة الحفظ',
    'knowledge.sample': 'محتوى نموذجي — ليس توثيقاً رسمياً',
    'knowledge.source': 'المصدر',
    'knowledge.back': 'عودة للقائمة',

    /* Projects */
    'projects.title': 'المشاريع',
    'projects.new': 'مشروع جديد',
    'projects.statusPlanning': 'قيد التخطيط',
    'projects.statusActive': 'قيد التنفيذ',
    'projects.statusPaused': 'متوقف مؤقتاً',
    'projects.statusDone': 'مكتمل',
    'projects.attachScripts': 'السكربتات المرتبطة',
    'projects.notes': 'ملاحظات المشروع',
    'projects.syncNote': 'المشاريع تُحفظ محلياً فقط — لا مزامنة بين الأجهزة',

    /* Reports */
    'reports.title': 'التقارير الأمنية',
    'reports.new': 'تقرير جديد',
    'reports.execSummary': 'الملخص التنفيذي',
    'reports.scope': 'النطاق',
    'reports.findings': 'النتائج',
    'reports.evidence': 'الأدلة',
    'reports.recommendations': 'التوصيات',
    'reports.references': 'المراجع',
    'reports.severity': 'الخطورة',
    'reports.addFinding': 'إضافة نتيجة',
    'reports.exportTxt': 'تصدير نص',
    'reports.exportJson': 'تصدير JSON',
    'reports.print': 'طباعة',
    'reports.disclaimer': 'كل النتائج يدوية. لا توجد فحوصات ماسحة. حدّد الخطورة بنفسك.',

    /* Repositories */
    'repos.title': 'البحث في المستودعات',
    'repos.subtitle': 'ابحث في قائمة محلية أو افتح بحث GitHub الرسمي',
    'repos.offline': 'وضع بدون اتصال',
    'repos.offlineDesc': 'لا يقوم التطبيق بأي طلبات شبكة. زر "بحث في GitHub" يفتح موقع GitHub في نافذة جديدة.',
    'repos.openGithub': 'فتح بحث GitHub',
    'repos.localList': 'قائمة محلية',
    'repos.liveSearch': 'البحث المباشر معطّل',
    'repos.liveSearchDesc': 'يتطلب خادم وسيط لمفتاح API — غير متاح في v1.0',
    'repos.importList': 'استيراد قائمة (JSON)',
    'repos.noLocal': 'لا توجد مستودعات محلية — استورد قائمة JSON أو استخدم زر GitHub',

    /* About */
    'about.title': 'حول NexSec AI',
    'about.version': 'الإصدار',
    'about.tagline': 'مساحة عمل تطوير الأمن السيبراني',
    'about.description': 'تطبيق أمامي كامل لتنظيم مشاريع الأمن السيبراني، حفظ السكربتات، وكتابة التقارير — يعمل بالكامل من متصفحك.',
    'about.limitations': 'القيود الحالية',
    'about.limitationsDesc': 'الذكاء الاصطناعي غير متصل. البحث المباشر غير متاح. التحليل التلقائي غير متاح. لا تنفيذ كود.',
    'about.privacy': 'الخصوصية',
    'about.privacyDesc': 'لا تتبّع. لا خوادم. لا إرسال بيانات. كل شيء محلي.',
    'about.license': 'الرخصة: MIT',

    /* Confirmations */
    'confirm.deleteScript': 'حذف هذا السكربت؟',
    'confirm.deleteProject': 'حذف هذا المشروع؟ سيتم إلغاء ربط السكربتات.',
    'confirm.deleteReport': 'حذف هذا التقرير؟',
    'confirm.deleteConversation': 'حذف هذه المحادثة؟',
    'confirm.clearConversation': 'تفريغ كل الرسائل في هذه المحادثة؟',
    'confirm.resetSettings': 'إعادة تعيين كل الإعدادات؟'
  },

  en: {
    /* App */
    'app.name': 'NexSec AI',
    'app.tagline': 'Your Cybersecurity Development Workspace',
    'app.version': 'Version 1.0 — Frontend-First',

    /* Nav */
    'nav.workspace': 'Workspace',
    'nav.library': 'Library',
    'nav.manage': 'Manage',
    'nav.system': 'System',
    'nav.dashboard': 'Dashboard',
    'nav.chat': 'Chat (Demo)',
    'nav.codeStudio': 'Code Studio',
    'nav.repos': 'Repository Search',
    'nav.scripts': 'Script Library',
    'nav.tools': 'Security Tools',
    'nav.knowledge': 'Knowledge Base',
    'nav.projects': 'Projects',
    'nav.reports': 'Security Reports',
    'nav.settings': 'Settings',
    'nav.about': 'About',

    /* Status */
    'status.ai': 'AI: Not Connected',
    'status.repo': 'Repository: Offline',
    'status.backend': 'Backend: Disabled',
    'status.aiLong': 'AI provider is not connected in this version',
    'status.repoLong': 'Live search is disabled — opens official GitHub search',
    'status.backendLong': 'No backend server connected',

    /* Common */
    'common.save': 'Save',
    'common.cancel': 'Cancel',
    'common.delete': 'Delete',
    'common.edit': 'Edit',
    'common.close': 'Close',
    'common.confirm': 'Confirm',
    'common.search': 'Search',
    'common.clear': 'Clear',
    'common.create': 'Create',
    'common.copy': 'Copy',
    'common.copied': 'Copied',
    'common.download': 'Download',
    'common.export': 'Export',
    'common.import': 'Import',
    'common.add': 'Add',
    'common.name': 'Name',
    'common.title': 'Title',
    'common.description': 'Description',
    'common.category': 'Category',
    'common.language': 'Language',
    'common.status': 'Status',
    'common.created': 'Created',
    'common.updated': 'Updated',
    'common.actions': 'Actions',
    'common.none': 'None',
    'common.loading': 'Loading…',
    'common.optional': 'Optional',
    'common.required': 'Required',
    'common.yes': 'Yes',
    'common.no': 'No',
    'common.na': 'N/A',
    'common.back': 'Back',
    'common.next': 'Next',
    'common.prev': 'Previous',
    'common.retry': 'Retry',
    'common.reset': 'Reset',
    'common.refresh': 'Refresh',
    'common.view': 'View',
    'common.open': 'Open',
    'common.apply': 'Apply',
    'common.filter': 'Filter',
    'common.sort': 'Sort',
    'common.all': 'All',
    'common.on': 'On',
    'common.off': 'Off',
    'common.ok': 'OK',
    'common.error': 'Error',
    'common.warning': 'Warning',
    'common.info': 'Info',
    'common.success': 'Success',
    'common.unknown': 'Unknown',
    'common.other': 'Other',
    'common.tags': 'Tags',
    'common.notes': 'Notes',
    'common.version': 'Version',
    'common.menu': 'Menu',
    'common.saved': 'Saved',
    'common.deleted': 'Deleted',
    'common.created_ok': 'Created',
    'common.updated_ok': 'Updated',
    'common.unsaved': 'Unsaved changes',
    'common.confirmDelete': 'Confirm deletion',
    'common.deleteWarning': 'This action cannot be undone.',
    'common.searchPlaceholder': 'Search…',
    'common.noResults': 'No results',
    'common.viewAll': 'View all',
    'common.quickActions': 'Quick actions',

    /* Empty states */
    'empty.scripts': 'No saved scripts yet',
    'empty.scriptsDesc': 'Use Code Studio or create a new script here',
    'empty.projects': 'No projects yet',
    'empty.projectsDesc': 'Create a new project to organize your work',
    'empty.reports': 'No reports yet',
    'empty.reportsDesc': 'Create a new security report',
    'empty.chats': 'No conversations yet',
    'empty.chatsDesc': 'Start a new conversation',
    'empty.search': 'No results for your search',
    'empty.searchDesc': 'Try other keywords or clear filters',
    'empty.generic': 'No content yet',
    'empty.toolsNotes': 'No notes for this tool',

    /* Errors */
    'error.storageUnavailable': 'Local storage unavailable — data will not persist',
    'error.storageQuota': 'Storage quota exceeded — delete some data',
    'error.generic': 'An unexpected error occurred',
    'error.notFound': 'Page not found',
    'error.notFoundDesc': 'Check the URL or return to Dashboard',
    'error.invalidFile': 'Invalid file — ensure it is a NexSec AI export',
    'error.required': 'This field is required',
    'error.tooShort': 'Text is too short',
    'error.tooLong': 'Text is too long',
    'error.aiUnavailable': 'AI is not connected',
    'error.aiUnavailableDesc': 'This feature requires an AI provider — not available in v1.0',
    'error.repoUnavailable': 'Live search is disabled',
    'error.repoUnavailableDesc': 'Use the official GitHub search button instead',
    'error.analysisUnavailable': 'Automated analysis unavailable',
    'error.analysisUnavailableDesc': 'Use the manual review checklist',

    /* Severity */
    'sev.info': 'Informational',
    'sev.low': 'Low',
    'sev.med': 'Medium',
    'sev.high': 'High',
    'sev.crit': 'Critical',

    /* Settings */
    'settings.title': 'Settings',
    'settings.language': 'Language',
    'settings.languageDesc': 'Choose interface language',
    'settings.theme': 'Theme',
    'settings.themeDesc': 'Dark or light',
    'settings.themeDark': 'Dark',
    'settings.themeLight': 'Light',
    'settings.fontSize': 'Font size',
    'settings.fontSizeDesc': 'Small / Medium / Large',
    'settings.fontSm': 'Small',
    'settings.fontMd': 'Medium',
    'settings.fontLg': 'Large',
    'settings.reduceMotion': 'Reduce motion',
    'settings.reduceMotionDesc': 'Disable animations',
    'settings.status': 'Connection status',
    'settings.privacy': 'Privacy',
    'settings.privacyDesc': 'All data is stored locally in your browser. No information is sent to any server.',
    'settings.reset': 'Reset settings',
    'settings.resetConfirm': 'Reset all settings to defaults?',
    'settings.clearData': 'Clear all local data',
    'settings.clearDataConfirm': 'This will delete all projects, scripts, reports, and conversations. This cannot be undone!',
    'settings.export': 'Export data',
    'settings.exportDesc': 'Download a JSON backup of all your data',
    'settings.import': 'Import data',
    'settings.importDesc': 'Restore from backup (replaces current data)',
    'settings.about': 'About',

    /* Dashboard */
    'dashboard.title': 'Dashboard',
    'dashboard.welcome': 'Welcome to NexSec AI',
    'dashboard.subtitle': 'Your Cybersecurity Development Workspace',
    'dashboard.projects': 'Projects',
    'dashboard.scripts': 'Scripts',
    'dashboard.reports': 'Reports',
    'dashboard.chats': 'Conversations',
    'dashboard.recentProjects': 'Recent Projects',
    'dashboard.recentScripts': 'Recent Scripts',
    'dashboard.recentReports': 'Recent Reports',
    'dashboard.quickStart': 'Quick Start',
    'dashboard.noRecent': 'None yet',

    /* Chat */
    'chat.title': 'Chat',
    'chat.new': 'New conversation',
    'chat.rename': 'Rename',
    'chat.delete': 'Delete conversation',
    'chat.clear': 'Clear conversation',
    'chat.placeholder': 'Type your message… (Enter to send, Shift+Enter for newline)',
    'chat.send': 'Send',
    'chat.aiNotConnected': 'AI Not Connected',
    'chat.aiNotConnectedDesc': 'Local demo mode. Messages are saved only — not sent to any model.',
    'chat.demoNotice': 'Local demo mode — no AI responses in v1.0',
    'chat.empty': 'Start a new conversation from the list',
    'chat.noConversation': 'No conversation selected',
    'chat.message': 'Message',
    'chat.messages': 'Messages',

    /* Code Studio */
    'code.title': 'Code Studio',
    'code.subtitle': 'Edit and save scripts safely',
    'code.editor': 'Editor',
    'code.titleField': 'Code title',
    'code.descField': 'Short description',
    'code.langField': 'Language',
    'code.lineCount': 'Lines',
    'code.charCount': 'Characters',
    'code.save': 'Save to Library',
    'code.saveDraft': 'Save Draft',
    'code.clear': 'Clear Editor',
    'code.clearConfirm': 'Clear the editor? Unsaved changes will be lost.',
    'code.explain': 'Explain Code',
    'code.explainUnavailable': 'Explanation unavailable until AI is connected',
    'code.review': 'Code Review',
    'code.reviewManual': 'Use the manual checklist below',
    'code.find': 'Find in Code',
    'code.findPlaceholder': 'Search text…',
    'code.noMatch': 'No match',
    'code.attachToProject': 'Attach to project',

    /* Scripts */
    'scripts.title': 'Script Library',
    'scripts.new': 'New Script',
    'scripts.filterLang': 'Filter by language',
    'scripts.filterCat': 'Filter by category',
    'scripts.sortBy': 'Sort by',
    'scripts.sortCreated': 'Creation date',
    'scripts.sortUpdated': 'Last modified',
    'scripts.favorite': 'Favorite',
    'scripts.unfavorite': 'Unfavorite',
    'scripts.warn': 'Warning: imported scripts are untrusted. Do not run without review.',

    /* Tools */
    'tools.title': 'Security Tools',
    'tools.subtitle': 'Educational reference for cybersecurity tools',
    'tools.docs': 'Official Docs',
    'tools.category': 'Category',
    'tools.platform': 'Platforms',
    'tools.license': 'License',
    'tools.notes': 'My Notes',
    'tools.bookmark': 'Bookmark',
    'tools.unbookmark': 'Remove Bookmark',
    'tools.disclaimer': 'Reference only. No tool is verified as installed or executed.',

    /* Knowledge */
    'knowledge.title': 'Knowledge Base',
    'knowledge.subtitle': 'Educational articles and references',
    'knowledge.categories': 'Categories',
    'knowledge.article': 'Article',
    'knowledge.readMore': 'Read more',
    'knowledge.bookmark': 'Bookmark',
    'knowledge.unbookmark': 'Remove Bookmark',
    'knowledge.sample': 'Sample content — not official documentation',
    'knowledge.source': 'Source',
    'knowledge.back': 'Back to list',

    /* Projects */
    'projects.title': 'Projects',
    'projects.new': 'New Project',
    'projects.statusPlanning': 'Planning',
    'projects.statusActive': 'In Progress',
    'projects.statusPaused': 'Paused',
    'projects.statusDone': 'Completed',
    'projects.attachScripts': 'Attached Scripts',
    'projects.notes': 'Project Notes',
    'projects.syncNote': 'Projects saved locally only — no cross-device sync',

    /* Reports */
    'reports.title': 'Security Reports',
    'reports.new': 'New Report',
    'reports.execSummary': 'Executive Summary',
    'reports.scope': 'Scope',
    'reports.findings': 'Findings',
    'reports.evidence': 'Evidence',
    'reports.recommendations': 'Recommendations',
    'reports.references': 'References',
    'reports.severity': 'Severity',
    'reports.addFinding': 'Add Finding',
    'reports.exportTxt': 'Export TXT',
    'reports.exportJson': 'Export JSON',
    'reports.print': 'Print',
    'reports.disclaimer': 'All findings are manual. No scans performed. Assign severity yourself.',

    /* Repositories */
    'repos.title': 'Repository Search',
    'repos.subtitle': 'Search local list or open official GitHub search',
    'repos.offline': 'Offline Mode',
    'repos.offlineDesc': 'This app makes no network requests. "Search GitHub" opens GitHub in a new tab.',
    'repos.openGithub': 'Open GitHub Search',
    'repos.localList': 'Local List',
    'repos.liveSearch': 'Live search disabled',
    'repos.liveSearchDesc': 'Requires backend proxy for API key — not available in v1.0',
    'repos.importList': 'Import List (JSON)',
    'repos.noLocal': 'No local repositories — import a JSON list or use GitHub button',

    /* About */
    'about.title': 'About NexSec AI',
    'about.version': 'Version',
    'about.tagline': 'Your Cybersecurity Development Workspace',
    'about.description': 'A complete frontend application for organizing cybersecurity projects, saving scripts, and writing reports — running entirely in your browser.',
    'about.limitations': 'Current Limitations',
    'about.limitationsDesc': 'AI is not connected. Live search unavailable. Automated analysis unavailable. No code execution.',
    'about.privacy': 'Privacy',
    'about.privacyDesc': 'No tracking. No servers. No data sent. Everything is local.',
    'about.license': 'License: MIT',

    /* Confirmations */
    'confirm.deleteScript': 'Delete this script?',
    'confirm.deleteProject': 'Delete this project? Attached scripts will be unlinked.',
    'confirm.deleteReport': 'Delete this report?',
    'confirm.deleteConversation': 'Delete this conversation?',
    'confirm.clearConversation': 'Clear all messages in this conversation?',
    'confirm.resetSettings': 'Reset all settings?'
  }
};

const i18n = {
  current: 'ar',

  t(key, params) {
    const dict = I18N[this.current] || I18N.ar;
    let str = dict[key];
    if (str == null) str = I18N.ar[key];
    if (str == null) str = I18N.en[key];
    if (str == null) return key;
    if (params) {
      str = str.replace(/\{(\w+)\}/g, (_, k) =>
        params[k] != null ? String(params[k]) : `{${k}}`);
    }
    return str;
  },

  applyToDOM() {
    $$('[data-i18n]').forEach(node => {
      const key = node.getAttribute('data-i18n');
      node.textContent = this.t(key);
    });
    $$('[data-i18n-placeholder]').forEach(node => {
      node.setAttribute('placeholder', this.t(node.getAttribute('data-i18n-placeholder')));
    });
    $$('[data-i18n-title]').forEach(node => {
      node.setAttribute('title', this.t(node.getAttribute('data-i18n-title')));
    });
    $$('[data-i18n-aria-label]').forEach(node => {
      node.setAttribute('aria-label', this.t(node.getAttribute('data-i18n-aria-label')));
    });
  },

  async setLang(lang) {
    if (!I18N[lang]) return;
    this.current = lang;
    document.documentElement.lang = lang;
    document.documentElement.dir = lang === 'ar' ? 'rtl' : 'ltr';

    const langLabel = $('#langLabel');
    if (langLabel) langLabel.textContent = lang === 'ar' ? 'EN' : 'AR';

    this.applyToDOM();
    saveSettings({ lang });
    State.emit('lang:changed', lang);

    Router.refresh();
  },

  toggle() {
    this.setLang(this.current === 'ar' ? 'en' : 'ar');
  }
};

const t = (key, params) => i18n.t(key, params);

/* ═══════════════════════════════════════════════════════════════
   4. SETTINGS
   ═══════════════════════════════════════════════════════════════ */

const DEFAULT_SETTINGS = Object.freeze({
  lang: 'ar',
  theme: 'dark',
  fontSize: 'md',
  reduceMotion: false
});

function loadSettings() {
  const stored = Storage.get('settings', null);
  return { ...DEFAULT_SETTINGS, ...(stored || {}) };
}

function saveSettings(partial) {
  const next = { ...loadSettings(), ...partial };
  const ok = Storage.set('settings', next);
  if (!ok) showToast(t('error.storageQuota'), 'warn');
  return next;
}

function resetSettings() {
  Storage.set('settings', { ...DEFAULT_SETTINGS });
  applySettingsToDOM({ ...DEFAULT_SETTINGS });
}

function applySettingsToDOM(settings) {
  const s = settings || loadSettings();
  document.documentElement.dataset.theme = s.theme || 'dark';
  document.documentElement.dataset.fontSize = s.fontSize || 'md';
  document.documentElement.lang = s.lang || 'ar';
  document.documentElement.dir = (s.lang === 'ar') ? 'rtl' : 'ltr';
  if (s.reduceMotion) document.documentElement.style.setProperty('--motion-off', '1');
  else document.documentElement.style.removeProperty('--motion-off');
}

/* ═══════════════════════════════════════════════════════════════
   5. STATE
   ═══════════════════════════════════════════════════════════════ */

const State = (() => {
  const listeners = new Map();

  return {
    on(event, fn) {
      if (!listeners.has(event)) listeners.set(event, new Set());
      listeners.get(event).add(fn);
      return () => {
        const set = listeners.get(event);
        if (set) set.delete(fn);
      };
    },
    emit(event, payload) {
      const set = listeners.get(event);
      if (!set) return;
      for (const fn of Array.from(set)) {
        try { fn(payload); }
        catch (err) { console.error(`[State:${event}]`, err); }
      }
    }
  };
})();

/* ═══════════════════════════════════════════════════════════════
   6. TOAST
   ═══════════════════════════════════════════════════════════════ */

const TOAST_ICONS = {
  ok: '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true"><path d="M20 6 9 17l-5-5"/></svg>',
  warn: '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true"><path d="M10.29 3.86 1.82 18a2 2 0 0 0 1.71 3h16.94a2 2 0 0 0 1.71-3L13.71 3.86a2 2 0 0 0-3.42 0z"/><line x1="12" y1="9" x2="12" y2="13"/><line x1="12" y1="17" x2="12.01" y2="17"/></svg>',
  err: '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true"><circle cx="12" cy="12" r="10"/><line x1="15" y1="9" x2="9" y2="15"/><line x1="9" y1="9" x2="15" y2="15"/></svg>',
  info: '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true"><circle cx="12" cy="12" r="10"/><line x1="12" y1="16" x2="12" y2="12"/><line x1="12" y1="8" x2="12.01" y2="8"/></svg>'
};

function showToast(message, type = 'info', duration = 4000) {
  const wrap = $('#toastWrap');
  if (!wrap) return null;
  const kind = ['ok', 'warn', 'err', 'info'].includes(type) ? type : 'info';

  const toast = el('div', { class: `toast toast-${kind}`, role: 'alert' });
  toast.innerHTML = TOAST_ICONS[kind] + `<div style="flex:1">${escapeHtml(message)}</div>`;

  const close = el('button', {
    class: 'toast__close',
    type: 'button',
    'aria-label': t('common.close'),
    onClick: () => toast.remove()
  }, '×');
  toast.appendChild(close);

  wrap.appendChild(toast);

  if (duration > 0) {
    setTimeout(() => { toast.style.opacity = '0'; setTimeout(() => toast.remove(), 200); }, duration);
  }
  return toast;
}

/* ═══════════════════════════════════════════════════════════════
   7. MODAL
   ═══════════════════════════════════════════════════════════════ */

let _activeModalCleanup = null;

function openModal({ title, content, actions = [], onClose } = {}) {
  closeActiveModal();

  const root = $('#modalRoot');
  const previousFocus = document.activeElement;
  let closed = false;

  const modal = el('div', {
    class: 'modal',
    role: 'dialog',
    'aria-modal': 'true',
    'aria-labelledby': title ? 'modalTitle' : undefined
  });

  if (title) {
    modal.appendChild(el('h2', { class: 'modal-title', id: 'modalTitle', text: title }));
  }

  if (content != null) {
    const body = el('div');
    if (typeof content === 'string') body.innerHTML = content;
    else body.appendChild(content);
    modal.appendChild(body);
  }

  if (actions.length) {
    const bar = el('div', { class: 'modal-actions' });
    for (const action of actions) {
      const btn = el('button', {
        type: 'button',
        class: 'btn ' + (action.class || ''),
        onClick: () => {
          if (action.onClick) action.onClick(close);
          else close();
        }
      }, action.label);
      bar.appendChild(btn);
    }
    modal.appendChild(bar);
  }

  const back = el('div', { class: 'modal-back' }, modal);
  back.addEventListener('click', (e) => {
    if (e.target === back) close();
  });

  function onKey(e) {
    if (e.key === 'Escape') { e.preventDefault(); close(); return; }
    if (e.key === 'Tab') {
      const focusable = modal.querySelectorAll(
        'button:not([disabled]), input:not([disabled]), select:not([disabled]), textarea:not([disabled]), a[href], [tabindex]:not([tabindex="-1"])'
      );
      if (!focusable.length) return;
      const first = focusable[0];
      const last = focusable[focusable.length - 1];
      if (e.shiftKey && document.activeElement === first) {
        e.preventDefault(); last.focus();
      } else if (!e.shiftKey && document.activeElement === last) {
        e.preventDefault(); first.focus();
      }
    }
  }

  function close() {
    if (closed) return;
    closed = true;
    document.removeEventListener('keydown', onKey);
    back.remove();
    _activeModalCleanup = null;
    if (previousFocus && typeof previousFocus.focus === 'function') {
      try { previousFocus.focus(); } catch {}
    }
    if (typeof onClose === 'function') onClose();
  }

  root.appendChild(back);
  document.addEventListener('keydown', onKey);
  _activeModalCleanup = close;

  setTimeout(() => {
    const target = modal.querySelector(
      'input:not([disabled]), select:not([disabled]), textarea:not([disabled]), button'
    );
    if (target) target.focus();
  }, 60);

  return close;
}

function closeActiveModal() {
  if (_activeModalCleanup) _activeModalCleanup();
}

function confirmDialog({ title, message, confirmLabel, cancelLabel, danger = false }) {
  return new Promise(resolve => {
    openModal({
      title: title || t('common.confirmDelete'),
      content: el('p', { class: 'modal-desc', text: message || '' }),
      actions: [
        {
          label: cancelLabel || t('common.cancel'),
          onClick: (close) => { close(); resolve(false); }
        },
        {
          label: confirmLabel || t('common.confirm'),
          class: danger ? 'btn-danger' : 'btn-primary',
          onClick: (close) => { close(); resolve(true); }
        }
      ],
      onClose: () => resolve(false)
    });
  });
}

/* ═══════════════════════════════════════════════════════════════
   8. ROUTER
   ═══════════════════════════════════════════════════════════════ */

const Router = (() => {
  const routes = {};
  let currentRoute = null;
  let currentParams = {};

  function register(path, handler) {
    routes[path] = handler;
  }

  function parseHash() {
    const raw = location.hash.replace(/^#\/?/, '') || 'dashboard';
    const [pathPart, queryPart = ''] = raw.split('?');
    const path = pathPart.replace(/\/+$/, '') || 'dashboard';
    let params = {};
    try {
      const usp = new URLSearchParams(queryPart);
      for (const [k, v] of usp.entries()) params[k] = v;
    } catch {}
    return { path, params };
  }

  function updateActiveNav(path) {
    $$('.nav-link').forEach(link => {
      const target = link.getAttribute('data-route');
      if (target === path) link.setAttribute('aria-current', 'page');
      else link.removeAttribute('aria-current');
    });
  }

  function renderError(main, err) {
    console.error('[Router]', err);
    main.innerHTML = '';
    const page = el('div', { class: 'page' });
    page.appendChild(el('div', { class: 'empty' },
      el('div', { class: 'empty__title', text: t('error.generic') }),
      el('div', { class: 'empty__desc', text: String(err?.message || err) })
    ));
    main.appendChild(page);
  }

  async function resolve() {
    const { path, params } = parseHash();
    currentRoute = path;
    currentParams = params;

    const main = $('#appMain');
    if (!main) return;

    updateActiveNav(path);

    if (document.body.dataset.drawer === 'open') {
      document.body.dataset.drawer = 'closed';
    }

    const handler = routes[path] || routes['404'];
    if (!handler) {
      main.innerHTML = '';
      main.appendChild(el('div', { class: 'page' },
        el('div', { class: 'empty' },
          el('div', { class: 'empty__title', text: t('error.notFound') }),
          el('div', { class: 'empty__desc', text: t('error.notFoundDesc') })
        )
      ));
      return;
    }

    window.scrollTo({ top: 0, behavior: 'auto' });

    try {
      await handler(main, params);
      main.focus({ preventScroll: true });
    } catch (err) {
      renderError(main, err);
    }
  }

  function navigate(path, params) {
    const qs = params && Object.keys(params).length
      ? '?' + new URLSearchParams(params).toString()
      : '';
    location.hash = '#/' + path + qs;
  }

  function refresh() { return resolve(); }

  function start() {
    window.addEventListener('hashchange', () => resolve());
    if (!location.hash) {
      history.replaceState(null, '', '#/dashboard');
    }
    resolve();
  }

  return {
    register, start, refresh, navigate,
    get current() { return currentRoute; },
    get params() { return currentParams; }
  };
})();

/* ═══════════════════════════════════════════════════════════════
   9. SHELL EVENTS
   ═══════════════════════════════════════════════════════════════ */

function initShellEvents() {
  const langBtn = $('#langToggle');
  if (langBtn) langBtn.addEventListener('click', () => i18n.toggle());

  const sidebarBtn = $('#sidebarToggle');
  if (sidebarBtn) {
    sidebarBtn.addEventListener('click', () => {
      const collapsed = document.body.dataset.sidebar === 'collapsed';
      document.body.dataset.sidebar = collapsed ? 'expanded' : 'collapsed';
      sidebarBtn.setAttribute('aria-expanded', String(collapsed));
      sidebarBtn.setAttribute('aria-label', collapsed ? 'طي الشريط الجانبي' : 'توسيع الشريط الجانبي');
    });
  }

  const menuBtn = $('#menuToggle');
  if (menuBtn) {
    menuBtn.addEventListener('click', () => {
      const open = document.body.dataset.drawer === 'open';
      document.body.dataset.drawer = open ? 'closed' : 'open';
      menuBtn.setAttribute('aria-expanded', String(!open));
    });
  }

  document.addEventListener('click', (e) => {
    if (document.body.dataset.drawer !== 'open') return;
    if (e.target.closest('#appSidebar')) return;
    if (e.target.closest('#menuToggle')) return;
    document.body.dataset.drawer = 'closed';
    if (menuBtn) menuBtn.setAttribute('aria-expanded', 'false');
  });

  document.addEventListener('keydown', (e) => {
    if (e.key === 'Escape' && document.body.dataset.drawer === 'open') {
      document.body.dataset.drawer = 'closed';
      if (menuBtn) {
        menuBtn.setAttribute('aria-expanded', 'false');
        menuBtn.focus();
      }
    }
  });

  window.addEventListener('beforeunload', (e) => {
    if (State._hasUnsaved) {
      e.preventDefault();
      e.returnValue = '';
    }
  });
}

/* ═══════════════════════════════════════════════════════════════
   10. DATA — الأدوات الأمنية
   ═══════════════════════════════════════════════════════════════ */

const DATA_TOOLS = [
  {
    id: 'nmap',
    name: 'Nmap',
    category: 'network',
    descAr: 'ماسح شبكات مفتوح المصدر لاستكشاف الأجهزة والخدمات المفتوحة. أداة أساسية لفحص المنافذ والتعرف على البنية الشبكية.',
    descEn: 'Open-source network scanner for host discovery and port/service identification. A foundational tool for network exploration.',
    docs: 'https://nmap.org/book/man.html',
    platforms: ['Linux', 'macOS', 'Windows'],
    license: 'NPSL (Nmap Public Source License)'
  },
  {
    id: 'wireshark',
    name: 'Wireshark',
    category: 'network',
    descAr: 'محلّل حزم شبكية رسومي لتحليل حركة المرور في الوقت الفعلي. أداة معيارية لتحليل البروتوكولات.',
    descEn: 'Graphical packet analyzer for real-time network traffic analysis. Industry standard for protocol inspection.',
    docs: 'https://www.wireshark.org/docs/',
    platforms: ['Linux', 'macOS', 'Windows'],
    license: 'GPLv2'
  },
  {
    id: 'burp',
    name: 'Burp Suite',
    category: 'web',
    descAr: 'منصة اختبار اختراق تطبيقات الويب من PortSwigger. تشمل نسخة مجتمعية ونسخة احترافية.',
    descEn: 'Web application security testing platform by PortSwigger. Community and Professional editions available.',
    docs: 'https://portswigger.net/burp/documentation',
    platforms: ['Linux', 'macOS', 'Windows'],
    license: 'Commercial (Community Edition free)'
  },
  {
    id: 'metasploit',
    name: 'Metasploit',
    category: 'exploit',
    descAr: 'إطار اختبار اختراق لتطوير وتنفيذ الاستغلالات. يُستخدم في اختبارات الاختراق الأخلاقي وفرق الأمن الدفاعي.',
    descEn: 'Penetration testing framework for developing and executing exploits. Used in ethical pentesting and defensive security.',
    docs: 'https://docs.metasploit.com/',
    platforms: ['Linux', 'macOS', 'Windows'],
    license: 'BSD-3-Clause (Framework)'
  },
  {
    id: 'nuclei',
    name: 'Nuclei',
    category: 'web',
    descAr: 'ماسح ثغرات سريع قائم على القوالب من ProjectDiscovery. قابل للتوسعة بقوالب YAML مخصصة.',
    descEn: 'Fast template-based vulnerability scanner by ProjectDiscovery. Extensible via custom YAML templates.',
    docs: 'https://docs.projectdiscovery.io/tools/nuclei/overview',
    platforms: ['Linux', 'macOS', 'Windows'],
    license: 'MIT'
  },
  {
    id: 'yara',
    name: 'YARA',
    category: 'malware',
    descAr: 'أداة لتصنيف وتحديد البرمجيات الخبيثة عبر قواعد نصية. معيار في تحليل البرمجيات الخبيثة.',
    descEn: 'Pattern-matching tool for malware identification and classification. Standard in malware analysis.',
    docs: 'https://yara.readthedocs.io/',
    platforms: ['Linux', 'macOS', 'Windows'],
    license: 'BSD-3-Clause'
  },
  {
    id: 'ghidra',
    name: 'Ghidra',
    category: 'reverse',
    descAr: 'إطار هندسة عكسية مفتوح المصدر من NSA. محلّل ثابت متقدم مع واجهة رسومية غنية.',
    descEn: 'Open-source reverse engineering framework by NSA. Advanced static analysis with rich GUI.',
    docs: 'https://ghidra-sre.org/',
    platforms: ['Linux', 'macOS', 'Windows'],
    license: 'Apache 2.0'
  },
  {
    id: 'zeek',
    name: 'Zeek',
    category: 'network',
    descAr: 'منصة مراقبة أمن الشبكات (سابقاً Bro). تحوّل حركة المرور إلى سجلات قابلة للتحليل.',
    descEn: 'Network security monitoring platform (formerly Bro). Turns traffic into structured logs for analysis.',
    docs: 'https://docs.zeek.org/',
    platforms: ['Linux', 'macOS'],
    license: 'BSD-3-Clause'
  },
  {
    id: 'suricata',
    name: 'Suricata',
    category: 'network',
    descAr: 'محرك كشف ومنع التسلل عالي الأداء. يدعم IDS/IPS/NSM مع دعم متعدد الخيوط.',
    descEn: 'High-performance IDS/IPS/NSM engine. Multi-threaded with rule-based detection.',
    docs: 'https://docs.suricata.io/',
    platforms: ['Linux', 'macOS', 'Windows'],
    license: 'GPLv2'
  },
  {
    id: 'semgrep',
    name: 'Semgrep',
    category: 'static',
    descAr: 'أداة تحليل كود ثابت خفيفة وسريعة. تدعم قواعد مخصصة لاكتشاف الأنماط الأمنية.',
    descEn: 'Lightweight, fast static analysis tool. Custom rules for detecting security patterns.',
    docs: 'https://semgrep.dev/docs/',
    platforms: ['Linux', 'macOS', 'Windows'],
    license: 'LGPL 2.1'
  },
  {
    id: 'bandit',
    name: 'Bandit',
    category: 'static',
    descAr: 'أداة تحليل أمني لكود Python من OpenStack. تكتشف المشاكل الأمنية الشائعة.',
    descEn: 'Python security linter by OpenStack. Detects common security issues.',
    docs: 'https://bandit.readthedocs.io/',
    platforms: ['Linux', 'macOS', 'Windows'],
    license: 'Apache 2.0'
  },
  {
    id: 'openssl',
    name: 'OpenSSL',
    category: 'crypto',
    descAr: 'مكتبة تشفير وأدوات سطر أوامر. تُستخدم لإدارة الشهادات والاتصالات الآمنة.',
    descEn: 'Cryptography library and CLI toolkit. Used for certificate management and secure connections.',
    docs: 'https://www.openssl.org/docs/',
    platforms: ['Linux', 'macOS', 'Windows'],
    license: 'Apache 2.0'
  },
  {
    id: 'trivy',
    name: 'Trivy',
    category: 'container',
    descAr: 'ماسح ثغرات للحاويات والتكوينات. يكتشف الثغرات في صور Docker وملفات IaC.',
    descEn: 'Vulnerability scanner for containers and configs. Detects issues in Docker images and IaC files.',
    docs: 'https://aquasecurity.github.io/trivy/',
    platforms: ['Linux', 'macOS', 'Windows'],
    license: 'Apache 2.0'
  },
  {
    id: 'zap',
    name: 'OWASP ZAP',
    category: 'web',
    descAr: 'أداة اختبار أمني لتطبيقات الويب من OWASP. مفتوحة المصدر مع واجهات رسومية وسطرية.',
    descEn: 'OWASP web application security testing tool. Open source with GUI and CLI interfaces.',
    docs: 'https://www.zaproxy.org/docs/',
    platforms: ['Linux', 'macOS', 'Windows'],
    license: 'Apache 2.0'
  }
];

const DATA_TOOL_CATEGORIES = [
  { id: 'network', labelAr: 'أمن الشبكات', labelEn: 'Network' },
  { id: 'web', labelAr: 'تطبيقات الويب', labelEn: 'Web Apps' },
  { id: 'exploit', labelAr: 'اختبار الاختراق', labelEn: 'Exploitation' },
  { id: 'malware', labelAr: 'تحليل البرمجيات الخبيثة', labelEn: 'Malware Analysis' },
  { id: 'reverse', labelAr: 'هندسة عكسية', labelEn: 'Reverse Engineering' },
  { id: 'static', labelAr: 'تحليل كود ثابت', labelEn: 'Static Analysis' },
  { id: 'crypto', labelAr: 'تشفير', labelEn: 'Cryptography' },
  { id: 'container', labelAr: 'حاويات', labelEn: 'Containers' }
];

/* ═══════════════════════════════════════════════════════════════
   11. DATA — قاعدة المعرفة
   ═══════════════════════════════════════════════════════════════ */

const DATA_KNOWLEDGE = [
  {
    id: 'net-01',
    category: 'network',
    titleAr: 'أساسيات أمن الشبكات',
    titleEn: 'Network Security Fundamentals',
    bodyAr: 'أمن الشبكات يهدف إلى حماية البيانات أثناء النقل والبنية التحتية للشبكة. يشمل المفاهيم الأساسية: تقسيم الشبكة (Segmentation)، جدران الحماية (Firewalls)، أنظمة كشف التسلل (IDS)، والاتصال المشفّر (TLS/SSH). المبدأ الذهبي هو "الثقة الصفرية" (Zero Trust): لا تثق بأي جهاز أو مستخدم تلقائياً حتى لو كان داخل الشبكة. من الممارسات الجيدة: تطبيق مبدأ أقل صلاحية، تسجيل الأحداث الأمنية مركزياً، وتحديث الأنظمة بانتظام.',
    bodyEn: 'Network security aims to protect data in transit and network infrastructure. Core concepts include segmentation, firewalls, intrusion detection systems (IDS), and encrypted communication (TLS/SSH). The golden principle is Zero Trust: trust no device or user automatically even inside the network. Best practices include applying the principle of least privilege, centralized security logging, and regular system updates.',
    source: 'محتوى تعليمي نموذجي / Sample educational content'
  },
  {
    id: 'web-01',
    category: 'web',
    titleAr: 'مقدمة عن أمن تطبيقات الويب',
    titleEn: 'Introduction to Web Application Security',
    bodyAr: 'أمن تطبيقات الويب يركّز على حماية المواقع من الهجمات الشائعة. الأصناف الأساسية حسب OWASP Top 10 تشمل: حقن SQL، XSS، فقدان التحكم في الوصول، والتصميم غير الآمن. المبدأ الأول: لا تثق بأي مدخل من المستخدم — تحقّق دائماً من جهة الخادم ومن جهة العميل. استخدم استعلامات مُعاملة (Parameterized Queries) بدلاً من تجميع السلاسل النصية، وهرّب أي محتوى يُعرض في المتصفح.',
    bodyEn: 'Web application security focuses on protecting sites from common attacks. OWASP Top 10 categories include SQL injection, XSS, broken access control, and insecure design. First principle: trust no user input — always validate on both server and client sides. Use parameterized queries instead of string concatenation, and escape any content rendered in the browser.',
    source: 'محتوى تعليمي نموذجي / Sample educational content'
  },
  {
    id: 'linux-01',
    category: 'linux',
    titleAr: 'تقوية أمن نظام Linux',
    titleEn: 'Linux Security Hardening',
    bodyAr: 'تقوية Linux تبدأ بخطوات أساسية: تعطيل تسجيل الدخول المباشر باسم root عبر SSH (منع PermitRootLogin)، استخدام مفاتيح SSH بدلاً من كلمات المرور، تفعيل جدار الحماية (ufw أو firewalld)، وتحديث الحزم بانتظام. أنظمة الملفات: تأكد من صلاحيات /etc/shadow (640 أو أقل) وملفات SSH. المراقبة: راجع /var/log/auth.log وjournalctl دورياً. SELinux أو AppArmor يضيفان طبقة حماية إضافية.',
    bodyEn: 'Linux hardening starts with basics: disable direct root SSH login (PermitRootLogin no), use SSH keys instead of passwords, enable the firewall (ufw or firewalld), and update packages regularly. Filesystems: ensure /etc/shadow has restricted permissions (640 or tighter) and SSH config is locked down. Monitoring: review /var/log/auth.log and journalctl regularly. SELinux or AppArmor add an extra defense layer.',
    source: 'محتوى تعليمي نموذجي / Sample educational content'
  },
  {
    id: 'windows-01',
    category: 'windows',
    titleAr: 'أمن أنظمة Windows',
    titleEn: 'Windows Security',
    bodyAr: 'أمن Windows يعتمد على طبقات متعددة: تفعيل BitLocker لتشفير الأقراص، ضبط سياسات Group Policy، تفعيل Windows Defender بكل ميزاته، وإدارة التحديثات عبر WSUS أو تحديثات تلقائية. الحسابات: استخدم حسابات مستخدم عادية للعمل اليومي، واحتفظ بحساب admin للطوارئ فقط. مراقبة الأحداث: Windows Event Viewer سجلّ أساسي — راقب Event ID 4625 (فشل تسجيل دخول) و4688 (عملية جديدة).',
    bodyEn: 'Windows security relies on multiple layers: enable BitLocker for disk encryption, configure Group Policy settings, enable Windows Defender fully, and manage updates via WSUS or automatic updates. Accounts: use standard user accounts for daily work, keep admin account only for emergencies. Event monitoring: Windows Event Viewer is a core log — watch Event ID 4625 (failed logon) and 4688 (new process).',
    source: 'محتوى تعليمي نموذجي / Sample educational content'
  },
  {
    id: 'defense-01',
    category: 'defense',
    titleAr: 'الأمن الدفاعي (Blue Team)',
    titleEn: 'Defensive Security (Blue Team)',
    bodyAr: 'الدفاع السيبراني يركّز على منع الكشف والاستجابة. يشمل: إدارة سجلات مركزية (SIEM)، مراقبة الشبكة (IDS/IPS)، إدارة الثغرات (Vulnerability Management)، الاستجابة للحوادث (Incident Response)، والاستخبارات عن التهديدات (Threat Intelligence). عملية IR نموذجية: التحضير → الكشف → الاحتواء → الاستئصال → الاستعادة → الدروس المستفادة. الأتمتة عبر SOAR تقلل زمن الاستجابة.',
    bodyEn: 'Cyber defense focuses on prevention, detection, and response. Includes centralized log management (SIEM), network monitoring (IDS/IPS), vulnerability management, incident response, and threat intelligence. Typical IR process: Preparation → Detection → Containment → Eradication → Recovery → Lessons learned. SOAR automation reduces response time.',
    source: 'محتوى تعليمي نموذجي / Sample educational content'
  },
  {
    id: 'forensics-01',
    category: 'forensics',
    titleAr: 'التحليل الجنائي الرقمي',
    titleEn: 'Digital Forensics',
    bodyAr: 'التحليل الجنائي الرقمي يهدف لاستخراج أدلة مقبولة قانونياً. مبادئ أساسية: الحفاظ على سلامة الدليل (Chain of Custody)، عدم تعديل الأصل، استخدام نسخ صور (Forensic Images) عبر أدوات مثل dd أو FTK Imager. تحليل: مساحات غير مخصصة، أرشيفات، سجلات النظام، الذاكرة (Memory Forensics بـ Volatility). التوثيق: كل خطوة موثّقة بتوقيت دقيق. الأدوات يجب أن تكون موثوقة ومختبرة.',
    bodyEn: 'Digital forensics aims to extract legally acceptable evidence. Core principles: maintain chain of custody, do not modify the original, use forensic images via tools like dd or FTK Imager. Analysis: unallocated space, archives, system logs, memory forensics (with Volatility). Documentation: every step documented with precise timestamps. Tools must be trusted and validated.',
    source: 'محتوى تعليمي نموذجي / Sample educational content'
  },
  {
    id: 'malware-01',
    category: 'malware',
    titleAr: 'مقدمة في تحليل البرمجيات الخبيثة',
    titleEn: 'Malware Analysis Introduction',
    bodyAr: 'تحليل البرمجيات الخبيثة نوعان: تحليل ساكن (Static) — فحص الكود دون تشغيله (strings، hashes، Disassembly). وتحليل حركي (Dynamic) — تشغيل العينة في بيئة معزولة (Sandbox) ومراقبة سلوكها. دائماً اعمل في بيئة معزولة (VM منفصلة، شبكة مقطوعة). لا تشغّل عينة خبيثة على جهازك الشخصي. أدوات شائعة: YARA للتصنيف، Ghidra/IDA للهندسة العكسية، Cuckoo/ANY.RUN للتحليل الديناميكي.',
    bodyEn: 'Malware analysis has two modes: static — inspecting code without running (strings, hashes, disassembly). Dynamic — running samples in an isolated sandbox and observing behavior. Always work in an isolated environment (separate VM, air-gapped network). Never run a malicious sample on your personal machine. Common tools: YARA for classification, Ghidra/IDA for reverse engineering, Cuckoo/ANY.RUN for dynamic analysis.',
    source: 'محتوى تعليمي نموذجي / Sample educational content'
  },
  {
    id: 'secure-01',
    category: 'secure-coding',
    titleAr: 'مبادئ البرمجة الآمنة',
    titleEn: 'Secure Coding Principles',
    bodyAr: 'البرمجة الآمنة تبدأ من مرحلة التصميم: التحقق من المدخلات (Input Validation)، الترميز الصحيح للمخرجات (Output Encoding)، فصل الصلاحيات (Authorization)، وإدارة الأخطاء بأمان دون كشف معلومات حساسة. تجنّب: eval، تنفيذ أوامر نظام من مدخلات المستخدم، تخزين كلمات مرور نصية، وتضمين أسرار في الكود. استخدم مكتبات موثوقة وحدّثها دورياً، وافحص الاعتماديات (SCA).',
    bodyEn: 'Secure coding starts at design: input validation, proper output encoding, authorization separation, and safe error handling that leaks no sensitive info. Avoid: eval, executing system commands from user input, storing plaintext passwords, and embedding secrets in code. Use trusted libraries and update them regularly, and scan dependencies (SCA).',
    source: 'محتوى تعليمي نموذجي / Sample educational content'
  },
  {
    id: 'vuln-01',
    category: 'vuln-mgmt',
    titleAr: 'إدارة الثغرات',
    titleEn: 'Vulnerability Management',
    bodyAr: 'إدارة الثغرات عملية مستمرة: اكتشاف (Scanning) → تقييم (Scoring بـ CVSS) → معالجة (Patch/Mitigate) → تحقق. الأدوات: Nessus، OpenVAS، Trivy. كل ثغرة تُصنّف حسب الخطورة والاستغلالية (Exploitability) والأثر (Impact). المخرجات: تقرير دوري للإدارة مع مؤشرات (MTTD، MTTR). التحديثات الطارئة تتم في غضون ساعات للثغرات الحرجة، والثغرات الأخرى تُعالَج وفق سياسة مكتوبة.',
    bodyEn: 'Vulnerability management is continuous: discovery (scanning) → assessment (CVSS scoring) → remediation (patch/mitigate) → verification. Tools: Nessus, OpenVAS, Trivy. Each vulnerability is classified by severity, exploitability, and impact. Outputs: periodic management report with metrics (MTTD, MTTR). Critical vulnerabilities get emergency patches within hours; others handled per written policy.',
    source: 'محتوى تعليمي نموذجي / Sample educational content'
  },
  {
    id: 'pentest-01',
    category: 'pentest',
    titleAr: 'أساسيات اختبار الاختراق',
    titleEn: 'Penetration Testing Fundamentals',
    bodyAr: 'اختبار الاختراق محاكاة معتمدة لهجوم على أنظمة بموافقة خطية مسبقة. المنهجية المعتمدة: الاستطلاع (Recon) → الفحص (Scanning) → الاستغلال (Exploitation) → ما بعد الاستغلال (Post-exploitation) → التقرير. الإطار القانوني أساسي: العقد، النطاق (Scope)، قواعد الاشتباك (Rules of Engagement). التفويض الخطي إلزامي — لا تختبر بدون إذن. التقرير يجب أن يوضّح الأدلة وخطوات إعادة الإنتاج بدقة.',
    bodyEn: 'Penetration testing is an authorized attack simulation with prior written consent. Standard methodology: Recon → Scanning → Exploitation → Post-exploitation → Reporting. Legal framework is essential: contract, scope, rules of engagement. Written authorization is mandatory — never test without permission. The report must clearly document evidence and precise reproduction steps.',
    source: 'محتوى تعليمي نموذجي / Sample educational content'
  }
];

const DATA_KNOWLEDGE_CATEGORIES = [
  { id: 'network', labelAr: 'أمن الشبكات', labelEn: 'Network Security' },
  { id: 'web', labelAr: 'أمن الويب', labelEn: 'Web Security' },
  { id: 'linux', labelAr: 'أمن Linux', labelEn: 'Linux Security' },
  { id: 'windows', labelAr: 'أمن Windows', labelEn: 'Windows Security' },
  { id: 'defense', labelAr: 'الدفاع السيبراني', labelEn: 'Defensive' },
  { id: 'forensics', labelAr: 'التحليل الجنائي', labelEn: 'Forensics' },
  { id: 'malware', labelAr: 'تحليل البرمجيات الخبيثة', labelEn: 'Malware Analysis' },
  { id: 'secure-coding', labelAr: 'البرمجة الآمنة', labelEn: 'Secure Coding' },
  { id: 'vuln-mgmt', labelAr: 'إدارة الثغرات', labelEn: 'Vulnerability Mgmt' },
  { id: 'pentest', labelAr: 'اختبار الاختراق', labelEn: 'Penetration Testing' }
];

/* ═══════════════════════════════════════════════════════════════
   12. DATA — أمثلة سكربتات
   ═══════════════════════════════════════════════════════════════ */

const DATA_EXAMPLES = [
  {
    id: 'py-hello-audit',
    title: 'Python: فحص صلاحيات ملف',
    lang: 'python',
    category: 'defensive',
    code: `import os
import stat

def check_file_permissions(path):
    st = os.stat(path)
    mode = stat.filemode(st.st_mode)
    readable = bool(st.st_mode & stat.S_IRUSR)
    writable = bool(st.st_mode & stat.S_IWUSR)
    executable = bool(st.st_mode & stat.S_IXUSR)
    return {
        'path': path,
        'mode': mode,
        'user_read': readable,
        'user_write': writable,
        'user_execute': executable
    }

if __name__ == '__main__':
    import sys
    target = sys.argv[1] if len(sys.argv) > 1 else '/etc/shadow'
    print(check_file_permissions(target))
`
  },
  {
    id: 'js-input-validation',
    title: 'JavaScript: التحقق من المدخلات',
    lang: 'javascript',
    category: 'secure-coding',
    code: `function validateInput(value) {
  if (typeof value !== 'string') return { ok: false, error: 'type' };
  const trimmed = value.trim();
  if (trimmed.length === 0) return { ok: false, error: 'empty' };
  if (trimmed.length > 200) return { ok: false, error: 'too_long' };
  // السماح فقط بالحروف والأرقام والشرطة والشرطة السفلية
  if (!/^[a-zA-Z0-9_-]+$/.test(trimmed)) {
    return { ok: false, error: 'invalid_chars' };
  }
  return { ok: true, value: trimmed };
}

console.log(validateInput('hello_world-123'));
console.log(validateInput('bad<script>'));
`
  },
  {
    id: 'bash-system-info',
    title: 'Bash: معلومات النظام',
    lang: 'bash',
    category: 'defensive',
    code: `#!/bin/bash
# معلومات أساسية عن النظام — للقراءة فقط

echo "=== النظام ==="
uname -a
echo "=== المستخدم الحالي ==="
whoami
echo "=== المستخدمون النشطون ==="
who
echo "=== آخر عمليات تسجيل دخول ==="
last -n 5
echo "=== قرص ==="
df -h
echo "=== الذاكرة ==="
free -h
`
  },
  {
    id: 'sql-safe-query',
    title: 'SQL: استعلام آمن (Parameterized)',
    lang: 'sql',
    category: 'secure-coding',
    code: `-- مثال مفاهيمي: استخدم دائماً Parameterized Queries
-- لا تبنِ الاستعلام بتجميع النصوص!

-- ✅ صحيح (في كود تطبيقك):
-- SELECT * FROM users WHERE email = ? AND active = 1;
--         ↑ يُمرَّر من معامل منفصل

-- ❌ خطأ:
-- 'SELECT * FROM users WHERE email = ' + userInput

-- الفهرسة والصلاحيات
CREATE INDEX idx_users_email ON users(email);

-- مبدأ أقل صلاحية
GRANT SELECT, INSERT ON users TO app_role;
-- ❌ لا تمنح DROP أو TRUNCATE بدون حاجة
`
  }
];

/* ═══════════════════════════════════════════════════════════════
   13. SERVICE — AI
   ═══════════════════════════════════════════════════════════════ */

const AIService = (() => {
  const config = {
    enabled: false,
    endpoint: null,
    model: null
  };

  function isConnected() {
    return config.enabled === true && !!config.endpoint;
  }

  function status() {
    if (isConnected()) return { state: 'connected', label: t('status.ai') };
    return { state: 'disconnected', label: t('status.ai'), reason: 'no_provider_configured' };
  }

  async function chat(_request) {
    if (!isConnected()) {
      return {
        ok: false,
        error: {
          code: 'AI_NOT_CONNECTED',
          message: t('error.aiUnavailableDesc')
        }
      };
    }
    return {
      ok: false,
      error: {
        code: 'AI_NOT_IMPLEMENTED',
        message: 'AI provider integration not implemented in v1.0'
      }
    };
  }

  function getConfig() { return { ...config }; }

  return { isConnected, status, chat, getConfig };
})();

/* ═══════════════════════════════════════════════════════════════
   14. SERVICE — Repository Search
   ═══════════════════════════════════════════════════════════════ */

const RepositoryService = (() => {
  const config = { liveSearchEnabled: false };

  function isLive() {
    return config.liveSearchEnabled === true;
  }

  function githubSearchUrl(query, language) {
    const params = new URLSearchParams();
    if (query) params.set('q', language ? `${query} language:${language}` : query);
    else if (language) params.set('q', `language:${language}`);
    params.set('type', 'repositories');
    return `https://github.com/search?${params.toString()}`;
  }

  function searchLocal(list, query, language) {
    if (!Array.isArray(list)) return [];
    const q = (query || '').trim().toLowerCase();
    const lang = (language || '').trim().toLowerCase();
    return list.filter(item => {
      if (!item) return false;
      if (lang && String(item.language || '').toLowerCase() !== lang) return false;
      if (!q) return true;
      const hay = [
        item.name, item.fullName, item.description, item.language, item.owner
      ].filter(Boolean).join(' ').toLowerCase();
      return hay.includes(q);
    });
  }

  async function searchLive(_query, _language) {
    if (!isLive()) {
      return {
        ok: false,
        error: {
          code: 'LIVE_SEARCH_DISABLED',
          message: t('repos.liveSearchDesc')
        }
      };
    }
    return { ok: false, error: { code: 'NOT_IMPLEMENTED', message: 'v1.0' } };
  }

  function getConfig() { return { ...config }; }

  return { isLive, githubSearchUrl, searchLocal, searchLive, getConfig };
})();

/* ═══════════════════════════════════════════════════════════════
   15. SERVICE — Analysis
   ═══════════════════════════════════════════════════════════════ */

const AnalysisService = (() => {
  async function analyze(_code, _lang) {
    return {
      ok: false,
      error: {
        code: 'ANALYSIS_UNAVAILABLE',
        message: t('error.analysisUnavailableDesc')
      }
    };
  }

  async function scan(_target) {
    return {
      ok: false,
      error: { code: 'SCAN_UNAVAILABLE', message: 'No scanner available in v1.0' }
    };
  }

  const REVIEW_CHECKLIST = Object.freeze([
    { id: 'rv-1', ar: 'تم التحقق من جميع مدخلات المستخدم (client + server)', en: 'All user inputs validated (client + server)' },
    { id: 'rv-2', ar: 'لا يوجد استخدام لـ eval أو تنفيذ كود ديناميكي', en: 'No eval or dynamic code execution' },
    { id: 'rv-3', ar: 'لا توجد أسرار في الكود (مفاتيح، كلمات مرور)', en: 'No secrets in code (keys, passwords)' },
    { id: 'rv-4', ar: 'الاستعلامات معاملة (parameterized) — لا تجميع نصوص', en: 'Queries parameterized — no string concatenation' },
    { id: 'rv-5', ar: 'الأخطاء لا تكشف معلومات حساسة', en: 'Errors do not leak sensitive info' },
    { id: 'rv-6', ar: 'الصلاحيات مُطبَّقة بشكل صحيح على كل إجراء', en: 'Authorization enforced on every action' },
    { id: 'rv-7', ar: 'جميع الاعتماديات محدّثة وموثوقة', en: 'All dependencies up-to-date and trusted' },
    { id: 'rv-8', ar: 'المخرجات مهرّبة/مرمّزة حسب السياق (HTML, URL, SQL)', en: 'Outputs escaped/encoded per context (HTML, URL, SQL)' },
    { id: 'rv-9', ar: 'لا توجد بيانات حساسة في السجلات', en: 'No sensitive data in logs' },
    { id: 'rv-10', ar: 'المراجعة تمت بواسطة شخص آخر (لا مؤلف فقط)', en: 'Reviewed by someone other than author' }
  ]);

  return { analyze, scan, REVIEW_CHECKLIST };
})();

/* ═══════════════════════════════════════════════════════════════
   16. HELPERS
   ═══════════════════════════════════════════════════════════════ */

function readList(key) {
  const val = Storage.get(key, []);
  return Array.isArray(val) ? val : [];
}

function writeList(key, list) {
  const ok = Storage.set(key, list);
  if (ok) State.emit(`data:${key}:changed`, list);
  else showToast(t('error.storageQuota'), 'warn');
  return ok;
}

function icon(name, size = 18) {
  const paths = {
    plus: '<line x1="12" y1="5" x2="12" y2="19"/><line x1="5" y1="12" x2="19" y2="12"/>',
    trash: '<polyline points="3 6 5 6 21 6"/><path d="M19 6v14a2 2 0 0 1-2 2H7a2 2 0 0 1-2-2V6m3 0V4a2 2 0 0 1 2-2h4a2 2 0 0 1 2 2v2"/>',
    edit: '<path d="M11 4H4a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2v-7"/><path d="M18.5 2.5a2.121 2.121 0 0 1 3 3L12 15l-4 1 1-4 9.5-9.5z"/>',
    copy: '<rect x="9" y="9" width="13" height="13" rx="2"/><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"/>',
    download: '<path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"/><polyline points="7 10 12 15 17 10"/><line x1="12" y1="15" x2="12" y2="3"/>',
    check: '<polyline points="20 6 9 17 4 12"/>',
    search: '<circle cx="11" cy="11" r="8"/><line x1="21" y1="21" x2="16.65" y2="16.65"/>',
    close: '<line x1="18" y1="6" x2="6" y2="18"/><line x1="6" y1="6" x2="18" y2="18"/>',
    send: '<line x1="22" y1="2" x2="11" y2="13"/><polygon points="22 2 15 22 11 13 2 9 22 2"/>',
    chat: '<path d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z"/>',
    folder: '<path d="M3 7a2 2 0 0 1 2-2h4l2 2h8a2 2 0 0 1 2 2v8a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"/>',
    file: '<path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/><polyline points="14 2 14 8 20 8"/>',
    alert: '<path d="M10.29 3.86 1.82 18a2 2 0 0 0 1.71 3h16.94a2 2 0 0 0 1.71-3L13.71 3.86a2 2 0 0 0-3.42 0z"/><line x1="12" y1="9" x2="12" y2="13"/><line x1="12" y1="17" x2="12.01" y2="17"/>',
    code: '<polyline points="16 18 22 12 16 6"/><polyline points="8 6 2 12 8 18"/>',
    tools: '<path d="M14.7 6.3a4 4 0 1 0 5 5L21 12l-9 9-9-9 9-9z"/>',
    book: '<path d="M4 19.5A2.5 2.5 0 0 1 6.5 17H20"/><path d="M6.5 2H20v20H6.5A2.5 2.5 0 0 1 4 19.5v-15A2.5 2.5 0 0 1 6.5 2z"/>',
    repo: '<path d="M3 7a2 2 0 0 1 2-2h4l2 2h8a2 2 0 0 1 2 2v8a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"/>'
  };
  const svg = document.createElementNS('http://www.w3.org/2000/svg', 'svg');
  svg.setAttribute('viewBox', '0 0 24 24');
  svg.setAttribute('fill', 'none');
  svg.setAttribute('stroke', 'currentColor');
  svg.setAttribute('stroke-width', '2');
  svg.setAttribute('width', String(size));
  svg.setAttribute('height', String(size));
  svg.setAttribute('aria-hidden', 'true');
  svg.innerHTML = paths[name] || '';
  return svg;
}

function iconBtn(name, label, onClick, cls = 'btn btn-ghost btn-sm btn-icon') {
  const btn = el('button', {
    type: 'button',
    class: cls,
    'aria-label': label,
    title: label,
    onClick
  });
  btn.appendChild(icon(name, 14));
  return btn;
}

/* ═══════════════════════════════════════════════════════════════
   17. MODULE — Dashboard
   ═══════════════════════════════════════════════════════════════ */

function renderDashboard(main) {
  main.innerHTML = '';

  const projects = readList('projects');
  const scripts = readList('scripts');
  const reports = readList('reports');
  const conversations = readList('conversations');

  const page = el('div', { class: 'page' });

  /* ── Hero ── */
  const hero = el('div', { class: 'hero' });
  const heroLogo = document.createElementNS('http://www.w3.org/2000/svg', 'svg');
  heroLogo.setAttribute('viewBox', '0 0 64 64');
  heroLogo.setAttribute('class', 'hero__logo');
  heroLogo.innerHTML = `
    <rect width="64" height="64" rx="14" fill="#0a0e12"/>
    <path d="M32 8 L52 16 L52 32 C52 44 42 54 32 58 C22 54 12 44 12 32 L12 16 Z" fill="none" stroke="#10b981" stroke-width="2.5" stroke-linejoin="round"/>
    <polygon points="32,20 42,25.5 42,37 32,42.5 22,37 22,25.5" fill="none" stroke="#34d399" stroke-width="1.8" stroke-linejoin="round"/>
    <circle cx="32" cy="31.5" r="3" fill="#34d399"/>
  `;
  hero.appendChild(heroLogo);

  const heroBody = el('div', { class: 'hero__body' });
  heroBody.appendChild(el('div', { class: 'hero__title', text: t('dashboard.welcome') }));
  heroBody.appendChild(el('div', { class: 'hero__sub', text: t('dashboard.subtitle') }));
  const badges = el('div', { class: 'row', style: { marginTop: 'var(--s-2)' } });
  badges.appendChild(el('span', { class: 'badge badge-err', text: t('status.ai') }));
  badges.appendChild(el('span', { class: 'badge', text: t('app.version') }));
  badges.appendChild(el('span', { class: 'badge', text: Storage.available() ? 'Local Storage ✓' : t('error.storageUnavailable') }));
  heroBody.appendChild(badges);
  hero.appendChild(heroBody);
  page.appendChild(hero);

  /* ── Stats ── */
  const stats = el('div', { class: 'grid grid-4' });
  const statDefs = [
    { key: 'projects', val: projects.length, route: 'projects', icon: 'folder' },
    { key: 'scripts', val: scripts.length, route: 'scripts', icon: 'file' },
    { key: 'reports', val: reports.length, route: 'reports', icon: 'file' },
    { key: 'chats', val: conversations.length, route: 'chat', icon: 'chat' }
  ];
  for (const s of statDefs) {
    const card = el('div', {
      class: 'card card-inter stat-card',
      role: 'button',
      tabindex: '0',
      onClick: () => Router.navigate(s.route),
      onKeydown: (e) => { if (e.key === 'Enter' || e.key === ' ') Router.navigate(s.route); }
    });
    const top = el('div', { class: 'row row-between' });
    top.appendChild(el('div', { class: 'stat__lbl', text: t('dashboard.' + s.key) }));
    top.appendChild(icon(s.icon, 16));
    card.appendChild(top);
    card.appendChild(el('div', { class: 'stat__val', text: String(s.val) }));
    stats.appendChild(card);
  }
  page.appendChild(stats);

  /* ── Quick actions ── */
  const quickCard = el('div', { class: 'card' });
  quickCard.appendChild(el('div', { class: 'card-title', text: t('dashboard.quickStart') }));
  const quickGrid = el('div', { class: 'grid grid-3' });
  const quickActions = [
    { label: t('nav.codeStudio'), icon: 'code', route: 'code-studio' },
    { label: t('nav.scripts'), icon: 'file', route: 'scripts' },
    { label: t('nav.tools'), icon: 'tools', route: 'tools' },
    { label: t('nav.repos'), icon: 'repo', route: 'repositories' },
    { label: t('nav.knowledge'), icon: 'book', route: 'knowledge' },
    { label: t('nav.projects'), icon: 'folder', route: 'projects' },
    { label: t('nav.reports'), icon: 'file', route: 'reports' },
    { label: t('nav.chat'), icon: 'chat', route: 'chat' },
    { label: t('nav.settings'), icon: 'alert', route: 'settings' }
  ];
  for (const qa of quickActions) {
    const b = el('button', {
      type: 'button',
      class: 'btn',
      style: { justifyContent: 'flex-start', padding: 'var(--s-3)' },
      onClick: () => Router.navigate(qa.route)
    });
    b.appendChild(icon(qa.icon, 16));
    b.appendChild(el('span', { text: qa.label }));
    quickGrid.appendChild(b);
  }
  quickCard.appendChild(quickGrid);
  page.appendChild(quickCard);

  /* ── Recent items ── */
  const recents = el('div', { class: 'grid grid-3' });
  recents.appendChild(buildRecentCard('recentProjects', projects, 'projects'));
  recents.appendChild(buildRecentCard('recentScripts', scripts, 'scripts'));
  recents.appendChild(buildRecentCard('recentReports', reports, 'reports'));
  page.appendChild(recents);

  main.appendChild(page);
}

function buildRecentCard(titleKey, items, route) {
  const card = el('div', { class: 'card' });
  const hdr = el('div', { class: 'card-hdr' });
  hdr.appendChild(el('div', { class: 'card-title', text: t('dashboard.' + titleKey) }));
  hdr.appendChild(el('a', {
    href: `#/${route}`,
    class: 'card-link',
    text: t('common.viewAll'),
    style: { fontSize: 'var(--fs-xs)' }
  }));
  card.appendChild(hdr);

  if (!items.length) {
    card.appendChild(el('div', { class: 'card-sub', text: t('dashboard.noRecent') }));
    return card;
  }

  const sorted = [...items].sort((a, b) => (b.updatedAt || b.createdAt || 0) - (a.updatedAt || a.createdAt || 0)).slice(0, 3);
  const list = el('div', { class: 'stack stack-sm' });
  for (const item of sorted) {
    const itemEl = el('div', {
      class: 'list-item',
      style: { cursor: 'pointer' },
      onClick: () => Router.navigate(route)
    });
    const mainEl = el('div', { class: 'list-item__main' });
    mainEl.appendChild(el('div', { class: 'list-item__title', text: item.title || item.name || t('common.unknown') }));
    mainEl.appendChild(el('div', { class: 'list-item__sub', text: formatRelative(item.updatedAt || item.createdAt) }));
    itemEl.appendChild(mainEl);
    list.appendChild(itemEl);
  }
  card.appendChild(list);
  return card;
}

/* ═══════════════════════════════════════════════════════════════
   18. MODULE — Chat
   ═══════════════════════════════════════════════════════════════ */

const ChatState = {
  activeId: null,
  searchQuery: ''
};

function getConversations() {
  const raw = readList('conversations');
  return raw.filter(c => c && c.id && Array.isArray(c.messages));
}

function saveConversations(list) {
  return writeList('conversations', list);
}

function createConversation() {
  const conversations = getConversations();
  const now = Date.now();
  const conv = {
    id: uid('c_'),
    title: i18n.current === 'ar' ? 'محادثة جديدة' : 'New conversation',
    messages: [],
    createdAt: now,
    updatedAt: now
  };
  conversations.unshift(conv);
  saveConversations(conversations);
  ChatState.activeId = conv.id;
  return conv;
}

function updateConversation(id, patch) {
  const list = getConversations();
  const idx = list.findIndex(c => c.id === id);
  if (idx === -1) return null;
  list[idx] = { ...list[idx], ...patch, updatedAt: Date.now() };
  saveConversations(list);
  return list[idx];
}

function deleteConversation(id) {
  const list = getConversations().filter(c => c.id !== id);
  saveConversations(list);
  if (ChatState.activeId === id) {
    ChatState.activeId = list.length ? list[0].id : null;
  }
}

function renderMessage(msg, index, convId) {
  const wrap = el('div', {
    class: `chat-msg chat-msg-${msg.role === 'user' ? 'user' : 'system'}`
  });

  const content = msg.content || '';
  const codeRe = /```([\w-]*)\n([\s\S]*?)```/g;
  let lastIndex = 0;
  let match;
  let hasCode = false;

  while ((match = codeRe.exec(content)) !== null) {
    hasCode = true;
    const before = content.slice(lastIndex, match.index);
    if (before) wrap.appendChild(el('div', { text: before, style: { whiteSpace: 'pre-wrap' } }));

    const lang = match[1] || 'text';
    const code = match[2];
    const block = el('div', { class: 'code-block', style: { marginTop: 'var(--s-2)' } });
    const pre = el('pre');
    pre.appendChild(el('code', { text: code }));
    block.appendChild(pre);
    const copyBtn = iconBtn('copy', t('common.copy'), async () => {
      const ok = await copyText(code);
      showToast(ok ? t('common.copied') : t('common.error'), ok ? 'ok' : 'err', 2000);
    }, 'code-block__copy');
    block.appendChild(copyBtn);
    wrap.appendChild(block);
    lastIndex = codeRe.lastIndex;
  }

  if (!hasCode) {
    wrap.appendChild(el('div', { text: content, style: { whiteSpace: 'pre-wrap' } }));
  } else if (lastIndex < content.length) {
    wrap.appendChild(el('div', { text: content.slice(lastIndex), style: { whiteSpace: 'pre-wrap' } }));
  }

  const meta = el('div', { class: 'chat-msg-meta' });
  meta.appendChild(el('span', { text: formatRelative(msg.ts || Date.now()) }));
  const actions = el('div', { class: 'chat-msg-actions' });
  actions.appendChild(el('button', {
    type: 'button',
    class: 'chat-msg-btn',
    text: t('common.copy'),
    onClick: async () => {
      const ok = await copyText(content);
      showToast(ok ? t('common.copied') : t('common.error'), ok ? 'ok' : 'err', 2000);
    }
  }));
  meta.appendChild(actions);
  wrap.appendChild(meta);

  return wrap;
}

function renderChat(main) {
  main.innerHTML = '';

  const conversations = getConversations();
  if (ChatState.activeId && !conversations.find(c => c.id === ChatState.activeId)) {
    ChatState.activeId = conversations.length ? conversations[0].id : null;
  }
  if (!ChatState.activeId && conversations.length) {
    ChatState.activeId = conversations[0].id;
  }

  const page = el('div', { class: 'page' });

  const hdr = el('div', { class: 'page-hdr' });
  const hdrMain = el('div', { class: 'page-hdr__main' });
  hdrMain.appendChild(el('h1', { class: 'page-title', text: t('chat.title') }));
  hdrMain.appendChild(el('div', { class: 'page-sub', text: t('chat.demoNotice') }));
  hdr.appendChild(hdrMain);

  const actions = el('div', { class: 'row' });
  actions.appendChild(el('button', {
    type: 'button',
    class: 'btn btn-primary',
    onClick: () => {
      createConversation();
      Router.refresh();
    }
  }, icon('plus', 16), document.createTextNode(' ' + t('chat.new'))));
  hdr.appendChild(actions);
  page.appendChild(hdr);

  const banner = el('div', { class: 'banner banner-warn' });
  banner.innerHTML = TOAST_ICONS.warn;
  const bannerBody = el('div', { style: { flex: 1 } });
  bannerBody.appendChild(el('div', { text: t('chat.aiNotConnected'), style: { fontWeight: 600, marginBottom: '4px' } }));
  bannerBody.appendChild(el('div', { text: t('chat.aiNotConnectedDesc'), style: { fontSize: 'var(--fs-xs)' } }));
  banner.appendChild(bannerBody);
  page.appendChild(banner);

  const layout = el('div', { class: 'chat-layout' });

  const sidebar = el('div', { class: 'chat-sidebar' });
  const searchWrap = el('div', { class: 'search-wrap' });
  searchWrap.innerHTML = '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" class="search-wrap__icon"><circle cx="11" cy="11" r="8"/><line x1="21" y1="21" x2="16.65" y2="16.65"/></svg>';
  const searchInput = el('input', {
    type: 'search',
    class: 'input',
    placeholder: t('common.searchPlaceholder'),
    'aria-label': t('common.search'),
    value: ChatState.searchQuery,
    onInput: debounce((e) => {
      ChatState.searchQuery = e.target.value;
      renderChatList();
    }, 200)
  });
  searchWrap.appendChild(searchInput);
  sidebar.appendChild(searchWrap);

  const listWrap = el('div', { class: 'chat-list', id: 'chatList' });
  sidebar.appendChild(listWrap);

  function renderChatList() {
    listWrap.innerHTML = '';
    let visible = conversations;
    const q = ChatState.searchQuery.trim().toLowerCase();
    if (q) {
      visible = conversations.filter(c => {
        if ((c.title || '').toLowerCase().includes(q)) return true;
        return (c.messages || []).some(m => (m.content || '').toLowerCase().includes(q));
      });
    }
    if (!visible.length) {
      listWrap.appendChild(el('div', { class: 'card-sub', style: { padding: 'var(--s-3)' }, text: t('empty.chats') }));
      return;
    }
    for (const conv of visible) {
      const isActive = conv.id === ChatState.activeId;
      const item = el('div', {
        class: 'chat-item' + (isActive ? ' chat-item-active' : ''),
        role: 'button',
        tabindex: '0',
        title: conv.title,
        onClick: () => {
          ChatState.activeId = conv.id;
          Router.refresh();
        },
        onKeydown: (e) => {
          if (e.key === 'Enter' || e.key === ' ') {
            ChatState.activeId = conv.id;
            Router.refresh();
          }
        }
      });
      const label = el('div', { text: truncate(conv.title, 28), style: { flex: 1, overflow: 'hidden', textOverflow: 'ellipsis', whiteSpace: 'nowrap' } });
      item.appendChild(label);
      item.appendChild(el('span', { text: String(conv.messages?.length || 0), style: { fontSize: 'var(--fs-xs)', color: 'var(--text-3)' } }));
      listWrap.appendChild(item);
    }
  }
  renderChatList();
  layout.appendChild(sidebar);

  const chatMain = el('div', { class: 'stack' });
  const active = conversations.find(c => c.id === ChatState.activeId);

  if (!active) {
    const empty = el('div', { class: 'empty' });
    const iconSvg = icon('chat', 40);
    iconSvg.setAttribute('class', 'empty__icon');
    empty.appendChild(iconSvg);
    empty.appendChild(el('div', { class: 'empty__title', text: t('empty.chats') }));
    empty.appendChild(el('div', { class: 'empty__desc', text: t('empty.chatsDesc') }));
    empty.appendChild(el('button', {
      type: 'button',
      class: 'btn btn-primary',
      onClick: () => { createConversation(); Router.refresh(); }
    }, document.createTextNode(t('chat.new'))));
    chatMain.appendChild(empty);
  } else {
    const toolbar = el('div', { class: 'row row-between' });
    const titleWrap = el('div', { style: { flex: 1, minWidth: 0 } });
    titleWrap.appendChild(el('div', { text: active.title, style: { fontWeight: 600, overflow: 'hidden', textOverflow: 'ellipsis', whiteSpace: 'nowrap' } }));
    titleWrap.appendChild(el('div', { text: formatRelative(active.updatedAt), style: { fontSize: 'var(--fs-xs)', color: 'var(--text-3)' } }));
    toolbar.appendChild(titleWrap);

    const toolbarActions = el('div', { class: 'row' });

    toolbarActions.appendChild(iconBtn('edit', t('chat.rename'), () => {
      const input = el('input', {
        type: 'text',
        class: 'input',
        value: active.title,
        maxlength: '80',
        'aria-label': t('chat.rename')
      });
      const close = openModal({
        title: t('chat.rename'),
        content: input,
        actions: [
          { label: t('common.cancel'), onClick: (c) => c() },
          {
            label: t('common.save'),
            class: 'btn-primary',
            onClick: (c) => {
              const val = input.value.trim();
              if (!val) return;
              updateConversation(active.id, { title: val });
              c();
              Router.refresh();
              showToast(t('common.saved'), 'ok', 2000);
            }
          }
        ]
      });
      setTimeout(() => input.focus(), 80);
      return close;
    }));

    toolbarActions.appendChild(iconBtn('download', t('common.export'), () => {
      const txt = `# ${active.title}\n\n` + active.messages.map(m =>
        `**[${m.role}]** ${formatDate(m.ts)}\n\n${m.content}\n\n---\n`
      ).join('');
      const ok = download(`nexsec-chat-${active.id}.md`, txt, 'text/markdown;charset=utf-8');
      if (ok) showToast(t('common.saved'), 'ok', 2000);
    }));

    toolbarActions.appendChild(iconBtn('trash', t('chat.delete'), async () => {
      const ok = await confirmDialog({
        title: t('confirm.deleteConversation'),
        message: t('common.deleteWarning'),
        danger: true,
        confirmLabel: t('common.delete')
      });
      if (ok) {
        deleteConversation(active.id);
        Router.refresh();
        showToast(t('common.deleted'), 'ok', 2000);
      }
    }));

    toolbar.appendChild(toolbarActions);
    chatMain.appendChild(toolbar);

    const msgsBox = el('div', { class: 'chat-msgs', role: 'log', 'aria-live': 'polite' });
    if (!active.messages.length) {
      msgsBox.appendChild(el('div', {
        class: 'chat-msg chat-msg-system',
        text: i18n.current === 'ar'
          ? 'المحادثة فارغة — اكتب رسالتك الأولى أدناه.'
          : 'Empty conversation — type your first message below.'
      }));
    } else {
      for (let i = 0; i < active.messages.length; i++) {
        msgsBox.appendChild(renderMessage(active.messages[i], i, active.id));
      }
    }
    chatMain.appendChild(msgsBox);

    const inputWrap = el('div', { class: 'stack stack-sm' });
    const textarea = el('textarea', {
      class: 'textarea',
      rows: '3',
      placeholder: t('chat.placeholder'),
      'aria-label': t('chat.placeholder'),
      style: { minHeight: '80px' }
    });

    const inputBar = el('div', { class: 'row row-between' });
    inputBar.appendChild(el('span', {
      style: { fontSize: 'var(--fs-xs)', color: 'var(--text-3)' },
      text: i18n.current === 'ar'
        ? 'Enter للإرسال، Shift+Enter لسطر جديد'
        : 'Enter to send, Shift+Enter for newline'
    }));

    const sendBtn = el('button', {
      type: 'button',
      class: 'btn btn-primary',
      onClick: sendMessage
    }, icon('send', 16), document.createTextNode(' ' + t('chat.send')));

    function sendMessage() {
      const text = textarea.value.trim();
      if (!text) return;
      const messages = [...(active.messages || [])];
      messages.push({ role: 'user', content: text, ts: Date.now() });
      updateConversation(active.id, { messages });
      textarea.value = '';
      Router.refresh();
    }

    textarea.addEventListener('keydown', (e) => {
      if (e.key === 'Enter' && !e.shiftKey) {
        e.preventDefault();
        sendMessage();
      }
    });

    inputBar.appendChild(sendBtn);
    inputWrap.appendChild(textarea);
    inputWrap.appendChild(inputBar);
    chatMain.appendChild(inputWrap);

    if (active.messages.length) {
      const clearRow = el('div', { class: 'row row-end' });
      clearRow.appendChild(el('button', {
        type: 'button',
        class: 'btn btn-danger btn-sm',
        text: t('chat.clear'),
        onClick: async () => {
          const ok = await confirmDialog({
            title: t('confirm.clearConversation'),
            message: t('common.deleteWarning'),
            danger: true,
            confirmLabel: t('common.clear')
          });
          if (ok) {
            updateConversation(active.id, { messages: [] });
            Router.refresh();
            showToast(t('common.saved'), 'ok', 2000);
          }
        }
      }));
      chatMain.appendChild(clearRow);
    }
  }

  layout.appendChild(chatMain);
  page.appendChild(layout);
  main.appendChild(page);
}

/* ═══════════════════════════════════════════════════════════════
   19. STORAGE HELPERS
   ═══════════════════════════════════════════════════════════════ */

function getScripts() { return readList('scripts'); }
function saveScripts(list) { return writeList('scripts', list); }
function getProjects() { return readList('projects'); }

function getToolBookmarks() {
  const v = Storage.get('tools.bookmarks', []);
  return Array.isArray(v) ? v : [];
}
function saveToolBookmarks(list) { return Storage.set('tools.bookmarks', list); }

function getToolNotes() {
  const v = Storage.get('tools.notes', {});
  return v && typeof v === 'object' ? v : {};
}
function saveToolNotes(obj) { return Storage.set('tools.notes', obj); }

function getKnowledgeBookmarks() {
  const v = Storage.get('knowledge.bookmarks', []);
  return Array.isArray(v) ? v : [];
}
function saveKnowledgeBookmarks(list) { return Storage.set('knowledge.bookmarks', list); }

function getRepoList() {
  const v = Storage.get('repos.local', []);
  return Array.isArray(v) ? v : [];
}
function saveRepoList(list) { return Storage.set('repos.local', list); }

/* ═══════════════════════════════════════════════════════════════
   20. LANGUAGES
   ═══════════════════════════════════════════════════════════════ */

const LANGUAGES = [
  { id: 'python', label: 'Python' },
  { id: 'javascript', label: 'JavaScript' },
  { id: 'html', label: 'HTML' },
  { id: 'css', label: 'CSS' },
  { id: 'bash', label: 'Bash' },
  { id: 'powershell', label: 'PowerShell' },
  { id: 'c', label: 'C' },
  { id: 'cpp', label: 'C++' },
  { id: 'go', label: 'Go' },
  { id: 'sql', label: 'SQL' }
];

function getLangLabel(id) {
  const found = LANGUAGES.find(l => l.id === id);
  return found ? found.label : (id || t('common.unknown'));
}

/* ═══════════════════════════════════════════════════════════════
   21. MODULE — Code Studio
   ═══════════════════════════════════════════════════════════════ */

const CodeStudioState = {
  title: '',
  description: '',
  language: 'python',
  code: '',
  dirty: false,
  findQuery: ''
};

function loadDraft() {
  const draft = Storage.get('codeStudio.draft', null);
  if (draft && typeof draft === 'object') {
    CodeStudioState.title = draft.title || '';
    CodeStudioState.description = draft.description || '';
    CodeStudioState.language = draft.language || 'python';
    CodeStudioState.code = draft.code || '';
  }
}

function saveDraft() {
  Storage.set('codeStudio.draft', {
    title: CodeStudioState.title,
    description: CodeStudioState.description,
    language: CodeStudioState.language,
    code: CodeStudioState.code,
    savedAt: Date.now()
  });
}

function clearDraft() {
  Storage.remove('codeStudio.draft');
  CodeStudioState.title = '';
  CodeStudioState.description = '';
  CodeStudioState.language = 'python';
  CodeStudioState.code = '';
  CodeStudioState.dirty = false;
  State._hasUnsaved = false;
}

function renderCodeStudio(main) {
  main.innerHTML = '';
  loadDraft();

  const page = el('div', { class: 'page' });
  const hdr = el('div', { class: 'page-hdr' });
  const hdrMain = el('div', { class: 'page-hdr__main' });
  hdrMain.appendChild(el('h1', { class: 'page-title', text: t('code.title') }));
  hdrMain.appendChild(el('div', { class: 'page-sub', text: t('code.subtitle') }));
  hdr.appendChild(hdrMain);

  const dirtyBadge = el('span', {
    class: 'badge badge-warn',
    text: t('common.unsaved'),
    style: { display: CodeStudioState.dirty ? 'inline-flex' : 'none' }
  });
  hdr.appendChild(dirtyBadge);
  page.appendChild(hdr);

  const banner = el('div', { class: 'banner banner-info' });
  banner.innerHTML = TOAST_ICONS.info;
  banner.appendChild(el('div', {
    text: i18n.current === 'ar'
      ? 'الكود لا يُنفَّذ ولا يُرسل لأي خادم. تحرير وحفظ محلي فقط.'
      : 'Code is never executed or sent to any server. Local editing only.',
    style: { fontSize: 'var(--fs-sm)' }
  }));
  page.appendChild(banner);

  const metaCard = el('div', { class: 'card' });
  const metaGrid = el('div', { class: 'grid grid-3' });

  const titleField = el('div', { class: 'field' });
  titleField.appendChild(el('label', { class: 'field__lbl', text: t('code.titleField') }));
  const titleInput = el('input', {
    type: 'text', class: 'input', maxlength: '100',
    value: CodeStudioState.title,
    placeholder: i18n.current === 'ar' ? 'مثال: فحص صلاحيات' : 'e.g., Permission check'
  });
  titleInput.addEventListener('input', (e) => {
    CodeStudioState.title = e.target.value;
    markDirty();
  });
  titleField.appendChild(titleInput);
  metaGrid.appendChild(titleField);

  const descField = el('div', { class: 'field' });
  descField.appendChild(el('label', { class: 'field__lbl', text: t('code.descField') }));
  const descInput = el('input', {
    type: 'text', class: 'input', maxlength: '200',
    value: CodeStudioState.description,
    placeholder: t('common.optional')
  });
  descInput.addEventListener('input', (e) => {
    CodeStudioState.description = e.target.value;
    markDirty();
  });
  descField.appendChild(descInput);
  metaGrid.appendChild(descField);

  const langField = el('div', { class: 'field' });
  langField.appendChild(el('label', { class: 'field__lbl', text: t('code.langField') }));
  const langSelect = el('select', { class: 'select' });
  for (const lang of LANGUAGES) {
    const opt = el('option', { value: lang.id, text: lang.label });
    if (lang.id === CodeStudioState.language) opt.setAttribute('selected', '');
    langSelect.appendChild(opt);
  }
  langSelect.addEventListener('change', (e) => {
    CodeStudioState.language = e.target.value;
    markDirty();
  });
  langField.appendChild(langSelect);
  metaGrid.appendChild(langField);

  metaCard.appendChild(metaGrid);
  page.appendChild(metaCard);

  const editorCard = el('div', { class: 'card' });
  const editorHdr = el('div', { class: 'card-hdr' });
  editorHdr.appendChild(el('div', { class: 'card-title', text: t('code.editor') }));

  const counters = el('div', { class: 'row', style: { gap: 'var(--s-3)', fontSize: 'var(--fs-xs)', color: 'var(--text-2)' } });
  const lineCount = el('span', { text: `0 ${t('code.lineCount')}` });
  const charCount = el('span', { text: `0 ${t('code.charCount')}` });
  counters.appendChild(lineCount);
  counters.appendChild(charCount);
  editorHdr.appendChild(counters);
  editorCard.appendChild(editorHdr);

  const textarea = el('textarea', {
    class: 'code-area',
    spellcheck: 'false',
    placeholder: i18n.current === 'ar' ? 'اكتب الكود هنا…' : 'Write code here…'
  });
  textarea.value = CodeStudioState.code;

  function updateCounts() {
    const code = textarea.value;
    const lines = code.length === 0 ? 0 : code.split('\n').length;
    lineCount.textContent = `${lines} ${t('code.lineCount')}`;
    charCount.textContent = `${code.length} ${t('code.charCount')}`;
  }
  updateCounts();

  let saveTimer = null;
  textarea.addEventListener('input', () => {
    CodeStudioState.code = textarea.value;
    updateCounts();
    markDirty();
    clearTimeout(saveTimer);
    saveTimer = setTimeout(() => { saveDraft(); }, 800);
  });

  textarea.addEventListener('keydown', (e) => {
    if (e.key === 'Tab') {
      e.preventDefault();
      const start = textarea.selectionStart;
      const end = textarea.selectionEnd;
      const val = textarea.value;
      textarea.value = val.slice(0, start) + '  ' + val.slice(end);
      textarea.selectionStart = textarea.selectionEnd = start + 2;
      CodeStudioState.code = textarea.value;
      markDirty();
      updateCounts();
    }
  });

  editorCard.appendChild(textarea);

  const findRow = el('div', { class: 'row', style: { marginTop: 'var(--s-2)' } });
  const findInput = el('input', {
    type: 'search', class: 'input',
    placeholder: t('code.findPlaceholder'),
    style: { maxWidth: '260px' }
  });
  const findResult = el('span', { style: { fontSize: 'var(--fs-xs)', color: 'var(--text-3)' } });
  findInput.addEventListener('input', debounce((e) => {
    const q = e.target.value;
    CodeStudioState.findQuery = q;
    if (!q.trim()) { findResult.textContent = ''; return; }
    const matches = (CodeStudioState.code.match(new RegExp(q.replace(/[.*+?^${}()|[\]\\]/g, '\\$&'), 'gi')) || []).length;
    findResult.textContent = matches === 0
      ? t('code.noMatch')
      : (i18n.current === 'ar' ? `${matches} نتيجة` : `${matches} match(es)`);
    findResult.style.color = matches ? 'var(--success)' : 'var(--error)';
  }, 200));
  findRow.appendChild(findInput);
  findRow.appendChild(findResult);
  editorCard.appendChild(findRow);

  const actions = el('div', { class: 'row row-between', style: { marginTop: 'var(--s-3)' } });
  const leftActions = el('div', { class: 'row' });

  leftActions.appendChild(el('button', {
    type: 'button', class: 'btn btn-ghost btn-sm',
    onClick: async () => {
      const ok = await copyText(CodeStudioState.code);
      showToast(ok ? t('common.copied') : t('common.error'), ok ? 'ok' : 'err', 2000);
    }
  }, icon('copy', 14), document.createTextNode(' ' + t('common.copy'))));

  leftActions.appendChild(el('button', {
    type: 'button', class: 'btn btn-ghost btn-sm',
    onClick: () => {
      const name = CodeStudioState.title || 'code';
      const ext = fileExtension(CodeStudioState.language);
      const filename = `${sanitizeFilename(name)}.${ext}`;
      const ok = download(filename, CodeStudioState.code, 'text/plain;charset=utf-8');
      if (ok) showToast(t('common.saved'), 'ok', 2000);
    }
  }, icon('download', 14), document.createTextNode(' ' + t('common.download'))));

  leftActions.appendChild(el('button', {
    type: 'button', class: 'btn btn-ghost btn-sm',
    onClick: async () => {
      if (!CodeStudioState.code.trim()) return;
      const ok = await confirmDialog({
        title: t('code.clear'),
        message: t('code.clearConfirm'),
        danger: true,
        confirmLabel: t('code.clear')
      });
      if (ok) {
        textarea.value = '';
        CodeStudioState.code = '';
        updateCounts();
        markDirty();
      }
    }
  }, document.createTextNode(t('code.clear'))));

  actions.appendChild(leftActions);

  const rightActions = el('div', { class: 'row' });
  rightActions.appendChild(el('button', {
    type: 'button', class: 'btn',
    onClick: () => { saveDraft(); showToast(t('common.saved'), 'ok', 2000); }
  }, document.createTextNode(t('code.saveDraft'))));

  rightActions.appendChild(el('button', {
    type: 'button', class: 'btn btn-primary',
    onClick: () => saveToLibrary()
  }, document.createTextNode(t('code.save'))));

  actions.appendChild(rightActions);
  editorCard.appendChild(actions);

  function saveToLibrary() {
    if (!CodeStudioState.code.trim()) {
      showToast(t('error.required'), 'warn', 2500);
      return;
    }
    const now = Date.now();
    const script = {
      id: uid('s_'),
      title: CodeStudioState.title.trim() || (i18n.current === 'ar' ? 'سكربت بدون عنوان' : 'Untitled script'),
      description: CodeStudioState.description.trim(),
      language: CodeStudioState.language,
      code: CodeStudioState.code,
      category: 'general',
      tags: [],
      notes: '',
      favorite: false,
      projectId: null,
      createdAt: now,
      updatedAt: now
    };
    const list = getScripts();
    list.unshift(script);
    if (saveScripts(list)) {
      clearDraft();
      State._hasUnsaved = false;
      if (dirtyBadge) dirtyBadge.style.display = 'none';
      showToast(t('common.saved'), 'ok', 2500);
      Router.navigate('scripts');
    }
  }

  function markDirty() {
    if (!CodeStudioState.dirty) {
      CodeStudioState.dirty = true;
      State._hasUnsaved = true;
      if (dirtyBadge) dirtyBadge.style.display = 'inline-flex';
    }
  }

  page.appendChild(editorCard);

  const reviewCard = el('div', { class: 'card' });
  reviewCard.appendChild(el('div', { class: 'card-title', text: t('code.review') }));
  reviewCard.appendChild(el('div', { class: 'card-sub', text: t('code.reviewManual') }));

  const checklist = el('div', { class: 'stack stack-sm', style: { marginTop: 'var(--s-2)' } });
  for (const item of AnalysisService.REVIEW_CHECKLIST) {
    const label = el('label', { class: 'checkbox' });
    const cb = el('input', { type: 'checkbox' });
    label.appendChild(cb);
    label.appendChild(el('span', {
      text: i18n.current === 'ar' ? item.ar : item.en,
      style: { fontSize: 'var(--fs-sm)' }
    }));
    checklist.appendChild(label);
  }
  reviewCard.appendChild(checklist);
  page.appendChild(reviewCard);

  const explainCard = el('div', { class: 'card' });
  explainCard.appendChild(el('div', { class: 'card-title', text: t('code.explain') }));
  const explainBanner = el('div', { class: 'banner banner-warn' });
  explainBanner.innerHTML = TOAST_ICONS.warn;
  explainBanner.appendChild(el('div', {
    text: t('code.explainUnavailable'),
    style: { fontSize: 'var(--fs-sm)' }
  }));
  explainCard.appendChild(explainBanner);
  page.appendChild(explainCard);

  main.appendChild(page);
}

/* ═══════════════════════════════════════════════════════════════
   22. MODULE — Repository Search
   ═══════════════════════════════════════════════════════════════ */

const RepoState = {
  query: '',
  language: ''
};

function renderRepositorySearch(main) {
  main.innerHTML = '';

  const page = el('div', { class: 'page' });
  const hdr = el('div', { class: 'page-hdr' });
  const hdrMain = el('div', { class: 'page-hdr__main' });
  hdrMain.appendChild(el('h1', { class: 'page-title', text: t('repos.title') }));
  hdrMain.appendChild(el('div', { class: 'page-sub', text: t('repos.subtitle') }));
  hdr.appendChild(hdrMain);
  page.appendChild(hdr);

  const banner = el('div', { class: 'banner banner-info' });
  banner.innerHTML = TOAST_ICONS.info;
  banner.appendChild(el('div', {
    text: t('repos.offlineDesc'),
    style: { fontSize: 'var(--fs-sm)' }
  }));
  page.appendChild(banner);

  const toolbar = el('div', { class: 'toolbar' });
  const searchWrap = el('div', { class: 'search-wrap', style: { flex: 1, minWidth: '200px' } });
  searchWrap.innerHTML = '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" class="search-wrap__icon"><circle cx="11" cy="11" r="8"/><line x1="21" y1="21" x2="16.65" y2="16.65"/></svg>';
  const searchInput = el('input', {
    type: 'search', class: 'input',
    placeholder: t('common.searchPlaceholder'),
    value: RepoState.query,
    onInput: debounce((e) => {
      RepoState.query = e.target.value;
      renderResults();
    }, 200)
  });
  searchWrap.appendChild(searchInput);
  toolbar.appendChild(searchWrap);

  const langSelect = el('select', { class: 'select', style: { maxWidth: '180px' } });
  langSelect.appendChild(el('option', { value: '', text: t('common.all') }));
  for (const lang of LANGUAGES) {
    const opt = el('option', { value: lang.id, text: lang.label });
    if (lang.id === RepoState.language) opt.setAttribute('selected', '');
    langSelect.appendChild(opt);
  }
  langSelect.addEventListener('change', (e) => {
    RepoState.language = e.target.value;
    renderResults();
  });
  toolbar.appendChild(langSelect);

  toolbar.appendChild(el('button', {
    type: 'button', class: 'btn btn-primary',
    onClick: () => {
      const url = RepositoryService.githubSearchUrl(RepoState.query, RepoState.language);
      window.open(url, '_blank', 'noopener,noreferrer');
    }
  }, document.createTextNode(t('repos.openGithub'))));

  page.appendChild(toolbar);

  const importRow = el('div', { class: 'row' });
  const fileInput = el('input', { type: 'file', accept: '.json,application/json', style: { display: 'none' } });
  fileInput.addEventListener('change', handleImport);
  importRow.appendChild(fileInput);
  importRow.appendChild(el('button', {
    type: 'button', class: 'btn btn-sm',
    onClick: () => fileInput.click()
  }, document.createTextNode(t('repos.importList'))));
  page.appendChild(importRow);

  const resultsWrap = el('div', { id: 'repoResults' });
  page.appendChild(resultsWrap);

  function renderResults() {
    resultsWrap.innerHTML = '';
    const local = getRepoList();

    if (!local.length) {
      const empty = el('div', { class: 'empty' });
      const eicon = icon('repo', 40);
      eicon.setAttribute('class', 'empty__icon');
      empty.appendChild(eicon);
      empty.appendChild(el('div', { class: 'empty__title', text: t('repos.noLocal') }));
      empty.appendChild(el('div', { class: 'empty__desc', text: t('repos.liveSearchDesc') }));
      resultsWrap.appendChild(empty);
      return;
    }

    const filtered = RepositoryService.searchLocal(local, RepoState.query, RepoState.language);
    if (!filtered.length) {
      resultsWrap.appendChild(el('div', { class: 'empty' },
        el('div', { class: 'empty__title', text: t('empty.search') }),
        el('div', { class: 'empty__desc', text: t('empty.searchDesc') })
      ));
      return;
    }

    const grid = el('div', { class: 'grid grid-2' });
    for (const repo of filtered) {
      const card = el('div', { class: 'card' });
      const title = el('div', { class: 'card-title', text: repo.name || repo.fullName || '—' });
      card.appendChild(title);

      if (repo.description) {
        card.appendChild(el('div', { class: 'card-sub', text: repo.description }));
      }

      const meta = el('div', { class: 'row', style: { gap: 'var(--s-2)', flexWrap: 'wrap', marginTop: 'var(--s-2)' } });
      if (repo.language) meta.appendChild(el('span', { class: 'badge', text: repo.language }));
      if (repo.stars != null) meta.appendChild(el('span', { class: 'badge', text: `★ ${repo.stars}` }));
      if (repo.license) meta.appendChild(el('span', { class: 'badge', text: repo.license }));
      if (repo.updatedAt) meta.appendChild(el('span', { class: 'badge', text: formatRelative(repo.updatedAt) }));
      card.appendChild(meta);

      if (repo.url) {
        const link = el('a', {
          href: repo.url,
          target: '_blank',
          rel: 'noopener noreferrer',
          class: 'card-link',
          style: { fontSize: 'var(--fs-xs)', marginTop: 'var(--s-2)' },
          text: repo.url
        });
        card.appendChild(link);
      }

      grid.appendChild(card);
    }
    resultsWrap.appendChild(grid);
  }
  renderResults();

  function handleImport(e) {
    const file = e.target.files?.[0];
    if (!file) return;
    const reader = new FileReader();
    reader.onload = () => {
      try {
        const parsed = safeJSON(reader.result, null);
        const list = Array.isArray(parsed) ? parsed
          : (parsed && Array.isArray(parsed.repositories)) ? parsed.repositories : null;
        if (!list) throw new Error('invalid');
        const validated = list.filter(r => r && (r.name || r.fullName));
        if (!validated.length) throw new Error('empty');
        saveRepoList(validated);
        showToast(`${t('common.saved')} (${validated.length})`, 'ok', 2500);
        renderResults();
      } catch {
        showToast(t('error.invalidFile'), 'err', 3000);
      }
    };
    reader.onerror = () => showToast(t('error.generic'), 'err', 3000);
    reader.readAsText(file, 'utf-8');
    fileInput.value = '';
  }

  main.appendChild(page);
}

/* ═══════════════════════════════════════════════════════════════
   23. MODULE — Script Library
   ═══════════════════════════════════════════════════════════════ */

const ScriptsState = {
  search: '',
  langFilter: '',
  catFilter: '',
  sortBy: 'updated',
  showFavoritesOnly: false
};

function renderScriptLibrary(main) {
  main.innerHTML = '';

  const page = el('div', { class: 'page' });
  const hdr = el('div', { class: 'page-hdr' });
  const hdrMain = el('div', { class: 'page-hdr__main' });
  hdrMain.appendChild(el('h1', { class: 'page-title', text: t('scripts.title') }));
  hdr.appendChild(hdrMain);
  hdr.appendChild(el('button', {
    type: 'button', class: 'btn btn-primary',
    onClick: () => openScriptEditor(null)
  }, icon('plus', 14), document.createTextNode(' ' + t('scripts.new'))));
  page.appendChild(hdr);

  const warn = el('div', { class: 'banner banner-warn' });
  warn.innerHTML = TOAST_ICONS.warn;
  warn.appendChild(el('div', { text: t('scripts.warn'), style: { fontSize: 'var(--fs-sm)' } }));
  page.appendChild(warn);

  const toolbar = el('div', { class: 'toolbar' });

  const searchWrap = el('div', { class: 'search-wrap', style: { flex: 1, minWidth: '180px' } });
  searchWrap.innerHTML = '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" class="search-wrap__icon"><circle cx="11" cy="11" r="8"/><line x1="21" y1="21" x2="16.65" y2="16.65"/></svg>';
  const searchInput = el('input', {
    type: 'search', class: 'input', placeholder: t('common.searchPlaceholder'),
    value: ScriptsState.search,
    onInput: debounce((e) => { ScriptsState.search = e.target.value; renderList(); }, 200)
  });
  searchWrap.appendChild(searchInput);
  toolbar.appendChild(searchWrap);

  const langSelect = el('select', { class: 'select', style: { maxWidth: '160px' } });
  langSelect.appendChild(el('option', { value: '', text: t('scripts.filterLang') }));
  for (const lang of LANGUAGES) {
    const opt = el('option', { value: lang.id, text: lang.label });
    if (lang.id === ScriptsState.langFilter) opt.setAttribute('selected', '');
    langSelect.appendChild(opt);
  }
  langSelect.addEventListener('change', (e) => { ScriptsState.langFilter = e.target.value; renderList(); });
  toolbar.appendChild(langSelect);

  const sortSelect = el('select', { class: 'select', style: { maxWidth: '180px' } });
  sortSelect.appendChild(el('option', { value: 'updated', text: t('scripts.sortUpdated') }));
  sortSelect.appendChild(el('option', { value: 'created', text: t('scripts.sortCreated') }));
  sortSelect.appendChild(el('option', { value: 'title', text: t('common.title') }));
  sortSelect.value = ScriptsState.sortBy;
  sortSelect.addEventListener('change', (e) => { ScriptsState.sortBy = e.target.value; renderList(); });
  toolbar.appendChild(sortSelect);

  toolbar.appendChild(el('button', {
    type: 'button', class: 'btn btn-sm',
    onClick: () => { ScriptsState.showFavoritesOnly = !ScriptsState.showFavoritesOnly; renderList(); },
    class: 'btn btn-sm' + (ScriptsState.showFavoritesOnly ? ' btn-primary' : '')
  }, document.createTextNode('★ ' + t('scripts.favorite'))));

  page.appendChild(toolbar);

  const listWrap = el('div', { id: 'scriptList' });
  page.appendChild(listWrap);

  function renderList() {
    listWrap.innerHTML = '';
    let scripts = getScripts();

    const q = ScriptsState.search.trim().toLowerCase();
    if (q) {
      scripts = scripts.filter(s =>
        (s.title || '').toLowerCase().includes(q) ||
        (s.description || '').toLowerCase().includes(q) ||
        (s.code || '').toLowerCase().includes(q)
      );
    }
    if (ScriptsState.langFilter) {
      scripts = scripts.filter(s => s.language === ScriptsState.langFilter);
    }
    if (ScriptsState.showFavoritesOnly) {
      scripts = scripts.filter(s => s.favorite);
    }

    scripts.sort((a, b) => {
      if (ScriptsState.sortBy === 'title') return (a.title || '').localeCompare(b.title || '');
      if (ScriptsState.sortBy === 'created') return (b.createdAt || 0) - (a.createdAt || 0);
      return (b.updatedAt || 0) - (a.updatedAt || 0);
    });

    if (!scripts.length) {
      const empty = el('div', { class: 'empty' });
      const eicon = icon('file', 40);
      eicon.setAttribute('class', 'empty__icon');
      empty.appendChild(eicon);
      empty.appendChild(el('div', { class: 'empty__title', text: q || ScriptsState.langFilter || ScriptsState.showFavoritesOnly ? t('empty.search') : t('empty.scripts') }));
      empty.appendChild(el('div', { class: 'empty__desc', text: q ? t('empty.searchDesc') : t('empty.scriptsDesc') }));
      empty.appendChild(el('button', {
        type: 'button', class: 'btn btn-primary',
        onClick: () => openScriptEditor(null)
      }, document.createTextNode(t('scripts.new'))));
      listWrap.appendChild(empty);
      return;
    }

    const stack = el('div', { class: 'stack' });
    for (const script of scripts) {
      stack.appendChild(buildScriptItem(script));
    }
    listWrap.appendChild(stack);
  }

  function buildScriptItem(script) {
    const item = el('div', { class: 'list-item' });
    const mainEl = el('div', { class: 'list-item__main' });

    const titleRow = el('div', { class: 'list-item__title' });
    if (script.favorite) titleRow.appendChild(el('span', { text: '★', style: { color: 'var(--warning)' } }));
    titleRow.appendChild(el('span', { text: script.title || t('common.unknown') }));
    titleRow.appendChild(el('span', { class: 'badge', text: getLangLabel(script.language) }));
    mainEl.appendChild(titleRow);

    if (script.description) {
      mainEl.appendChild(el('div', { class: 'list-item__sub', text: truncate(script.description, 120) }));
    }

    const meta = el('div', { class: 'list-item__sub', style: { color: 'var(--text-3)', fontSize: 'var(--fs-xs)' } });
    meta.textContent = `${formatRelative(script.updatedAt || script.createdAt)} · ${script.code ? script.code.split('\n').length : 0} ${t('code.lineCount')}`;
    mainEl.appendChild(meta);

    item.appendChild(mainEl);

    const actions = el('div', { class: 'list-item__actions' });
    actions.appendChild(iconBtn('edit', t('common.edit'), () => openScriptEditor(script)));
    actions.appendChild(iconBtn('copy', t('common.copy'), async () => {
      const ok = await copyText(script.code || '');
      showToast(ok ? t('common.copied') : t('common.error'), ok ? 'ok' : 'err', 2000);
    }));
    actions.appendChild(iconBtn('download', t('common.download'), () => {
      const ext = fileExtension(script.language);
      const filename = `${sanitizeFilename(script.title)}.${ext}`;
      const ok = download(filename, script.code || '', 'text/plain;charset=utf-8');
      if (ok) showToast(t('common.saved'), 'ok', 2000);
    }));
    actions.appendChild(iconBtn('alert', script.favorite ? t('scripts.unfavorite') : t('scripts.favorite'), () => {
      const list = getScripts();
      const idx = list.findIndex(s => s.id === script.id);
      if (idx !== -1) {
        list[idx].favorite = !list[idx].favorite;
        list[idx].updatedAt = Date.now();
        saveScripts(list);
        renderList();
      }
    }));
    actions.appendChild(iconBtn('trash', t('common.delete'), async () => {
      const ok = await confirmDialog({
        title: t('confirm.deleteScript'),
        message: t('common.deleteWarning'),
        danger: true,
        confirmLabel: t('common.delete')
      });
      if (ok) {
        const list = getScripts().filter(s => s.id !== script.id);
        saveScripts(list);
        renderList();
        showToast(t('common.deleted'), 'ok', 2000);
      }
    }));

    item.appendChild(actions);
    return item;
  }

  main.appendChild(page);
  renderList();
}

function openScriptEditor(existing) {
  const isEdit = !!existing;
  const script = existing ? { ...existing } : {
    id: uid('s_'),
    title: '',
    description: '',
    language: 'python',
    code: '',
    category: 'general',
    tags: [],
    notes: '',
    favorite: false,
    projectId: null,
    createdAt: Date.now(),
    updatedAt: Date.now()
  };

  const form = el('div', { class: 'stack' });

  const titleField = el('div', { class: 'field' });
  titleField.appendChild(el('label', { class: 'field__lbl', text: t('common.title') + ' *' }));
  const titleInput = el('input', { type: 'text', class: 'input', value: script.title, maxlength: '100', required: 'true' });
  titleField.appendChild(titleInput);
  form.appendChild(titleField);

  const descField = el('div', { class: 'field' });
  descField.appendChild(el('label', { class: 'field__lbl', text: t('common.description') }));
  const descInput = el('textarea', { class: 'textarea', rows: '2', maxlength: '300' });
  descInput.value = script.description || '';
  descField.appendChild(descInput);
  form.appendChild(descField);

  const langField = el('div', { class: 'field' });
  langField.appendChild(el('label', { class: 'field__lbl', text: t('common.language') }));
  const langSelect = el('select', { class: 'select' });
  for (const lang of LANGUAGES) {
    const opt = el('option', { value: lang.id, text: lang.label });
    if (lang.id === script.language) opt.setAttribute('selected', '');
    langSelect.appendChild(opt);
  }
  langField.appendChild(langSelect);
  form.appendChild(langField);

  const codeField = el('div', { class: 'field' });
  codeField.appendChild(el('label', { class: 'field__lbl', text: t('code.editor') }));
  const codeArea = el('textarea', { class: 'code-area', rows: '10', spellcheck: 'false', style: { minHeight: '180px' } });
  codeArea.value = script.code || '';
  codeField.appendChild(codeArea);
  form.appendChild(codeField);

  const close = openModal({
    title: isEdit ? t('common.edit') : t('scripts.new'),
    content: form,
    actions: [
      { label: t('common.cancel'), onClick: (c) => c() },
      {
        label: t('common.save'),
        class: 'btn-primary',
        onClick: (c) => {
          const title = titleInput.value.trim();
          if (!title) {
            titleInput.classList.add('input-error');
            titleInput.focus();
            return;
          }
          script.title = title;
          script.description = descInput.value.trim();
          script.language = langSelect.value;
          script.code = codeArea.value;
          script.updatedAt = Date.now();

          const list = getScripts();
          const idx = list.findIndex(s => s.id === script.id);
          if (idx === -1) list.unshift(script);
          else list[idx] = script;

          if (saveScripts(list)) {
            c();
            Router.refresh();
            showToast(isEdit ? t('common.updated_ok') : t('common.created_ok'), 'ok', 2000);
          }
        }
      }
    ]
  });

  setTimeout(() => titleInput.focus(), 80);
  return close;
}

/* ═══════════════════════════════════════════════════════════════
   24. MODULE — Security Tools
   ═══════════════════════════════════════════════════════════════ */

const ToolsState = {
  query: '',
  category: ''
};

function renderTools(main) {
  main.innerHTML = '';

  const page = el('div', { class: 'page' });
  const hdr = el('div', { class: 'page-hdr' });
  const hdrMain = el('div', { class: 'page-hdr__main' });
  hdrMain.appendChild(el('h1', { class: 'page-title', text: t('tools.title') }));
  hdrMain.appendChild(el('div', { class: 'page-sub', text: t('tools.subtitle') }));
  hdr.appendChild(hdrMain);
  page.appendChild(hdr);

  const disclaimer = el('div', { class: 'banner banner-info' });
  disclaimer.innerHTML = TOAST_ICONS.info;
  disclaimer.appendChild(el('div', { text: t('tools.disclaimer'), style: { fontSize: 'var(--fs-sm)' } }));
  page.appendChild(disclaimer);

  const toolbar = el('div', { class: 'toolbar' });
  const searchWrap = el('div', { class: 'search-wrap', style: { flex: 1, minWidth: '180px' } });
  searchWrap.innerHTML = '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" class="search-wrap__icon"><circle cx="11" cy="11" r="8"/><line x1="21" y1="21" x2="16.65" y2="16.65"/></svg>';
  const searchInput = el('input', {
    type: 'search', class: 'input', placeholder: t('common.searchPlaceholder'),
    value: ToolsState.query,
    onInput: debounce((e) => { ToolsState.query = e.target.value; renderToolsList(); }, 200)
  });
  searchWrap.appendChild(searchInput);
  toolbar.appendChild(searchWrap);

  const catSelect = el('select', { class: 'select', style: { maxWidth: '200px' } });
  catSelect.appendChild(el('option', { value: '', text: t('common.all') + ' — ' + t('tools.category') }));
  for (const cat of DATA_TOOL_CATEGORIES) {
    const opt = el('option', {
      value: cat.id,
      text: i18n.current === 'ar' ? cat.labelAr : cat.labelEn
    });
    if (cat.id === ToolsState.category) opt.setAttribute('selected', '');
    catSelect.appendChild(opt);
  }
  catSelect.addEventListener('change', (e) => { ToolsState.category = e.target.value; renderToolsList(); });
  toolbar.appendChild(catSelect);

  page.appendChild(toolbar);

  const gridWrap = el('div', { id: 'toolsGrid' });
  page.appendChild(gridWrap);

  function renderToolsList() {
    gridWrap.innerHTML = '';
    const q = ToolsState.query.trim().toLowerCase();
    let filtered = DATA_TOOLS.filter(tool => {
      if (ToolsState.category && tool.category !== ToolsState.category) return false;
      if (!q) return true;
      const hay = [tool.name, tool.descAr, tool.descEn, tool.license].join(' ').toLowerCase();
      return hay.includes(q);
    });

    if (!filtered.length) {
      gridWrap.appendChild(el('div', { class: 'empty' },
        el('div', { class: 'empty__title', text: t('empty.search') }),
        el('div', { class: 'empty__desc', text: t('empty.searchDesc') })
      ));
      return;
    }

    const bookmarks = getToolBookmarks();
    const notes = getToolNotes();
    const grid = el('div', { class: 'grid grid-2' });

    for (const tool of filtered) {
      const card = el('div', { class: 'card' });

      const hdrRow = el('div', { class: 'card-hdr' });
      hdrRow.appendChild(el('div', { class: 'card-title', text: tool.name }));

      const isBookmarked = bookmarks.includes(tool.id);
      hdrRow.appendChild(el('button', {
        type: 'button', class: 'btn btn-ghost btn-sm',
        title: isBookmarked ? t('tools.unbookmark') : t('tools.bookmark'),
        onClick: () => {
          const list = getToolBookmarks();
          const idx = list.indexOf(tool.id);
          if (idx === -1) list.push(tool.id);
          else list.splice(idx, 1);
          saveToolBookmarks(list);
          renderToolsList();
        },
        style: { color: isBookmarked ? 'var(--warning)' : 'var(--text-2)' }
      }, document.createTextNode(isBookmarked ? '★' : '☆')));
      card.appendChild(hdrRow);

      card.appendChild(el('div', {
        class: 'card-sub',
        text: i18n.current === 'ar' ? tool.descAr : tool.descEn
      }));

      const meta = el('div', { class: 'row', style: { flexWrap: 'wrap', gap: 'var(--s-1)' } });
      const cat = DATA_TOOL_CATEGORIES.find(c => c.id === tool.category);
      if (cat) meta.appendChild(el('span', { class: 'badge', text: i18n.current === 'ar' ? cat.labelAr : cat.labelEn }));
      if (tool.license) meta.appendChild(el('span', { class: 'badge', text: tool.license }));
      for (const p of tool.platforms) meta.appendChild(el('span', { class: 'chip', text: p, style: { cursor: 'default' } }));
      card.appendChild(meta);

      const footer = el('div', { class: 'card-footer' });
      if (tool.docs) {
        footer.appendChild(el('a', {
          href: tool.docs,
          target: '_blank',
          rel: 'noopener noreferrer',
          class: 'btn btn-sm',
          text: t('tools.docs'),
          style: { fontSize: 'var(--fs-xs)' }
        }));
      }

      footer.appendChild(el('button', {
        type: 'button', class: 'btn btn-ghost btn-sm',
        onClick: () => openToolNotes(tool)
      }, document.createTextNode('📝 ' + t('tools.notes'))));
      card.appendChild(footer);

      if (notes[tool.id]) {
        card.appendChild(el('div', {
          style: {
            fontSize: 'var(--fs-xs)', color: 'var(--text-2)',
            borderTop: '1px solid var(--border)',
            paddingTop: 'var(--s-2)', marginTop: 'var(--s-1)'
          },
          text: truncate(notes[tool.id], 120)
        }));
      }

      grid.appendChild(card);
    }

    gridWrap.appendChild(grid);
  }

  function openToolNotes(tool) {
    const notes = getToolNotes();
    const ta = el('textarea', { class: 'textarea', rows: '6', style: { minHeight: '120px' } });
    ta.value = notes[tool.id] || '';
    openModal({
      title: `${tool.name} — ${t('tools.notes')}`,
      content: ta,
      actions: [
        { label: t('common.cancel'), onClick: (c) => c() },
        {
          label: t('common.save'),
          class: 'btn-primary',
          onClick: (c) => {
            const list = getToolNotes();
            const val = ta.value.trim();
            if (val) list[tool.id] = val;
            else delete list[tool.id];
            saveToolNotes(list);
            c();
            renderToolsList();
            showToast(t('common.saved'), 'ok', 2000);
          }
        }
      ]
    });
    setTimeout(() => ta.focus(), 80);
  }

  main.appendChild(page);
  renderToolsList();
}

/* ═══════════════════════════════════════════════════════════════
   25. MODULE — Knowledge Base
   ═══════════════════════════════════════════════════════════════ */

const KnowledgeState = {
  query: '',
  category: ''
};

function renderKnowledge(main) {
  main.innerHTML = '';

  const page = el('div', { class: 'page' });
  const hdr = el('div', { class: 'page-hdr' });
  const hdrMain = el('div', { class: 'page-hdr__main' });
  hdrMain.appendChild(el('h1', { class: 'page-title', text: t('knowledge.title') }));
  hdrMain.appendChild(el('div', { class: 'page-sub', text: t('knowledge.subtitle') }));
  hdr.appendChild(hdrMain);
  page.appendChild(hdr);

  const banner = el('div', { class: 'banner banner-info' });
  banner.innerHTML = TOAST_ICONS.info;
  banner.appendChild(el('div', { text: t('knowledge.sample'), style: { fontSize: 'var(--fs-sm)' } }));
  page.appendChild(banner);

  const toolbar = el('div', { class: 'toolbar' });
  const searchWrap = el('div', { class: 'search-wrap', style: { flex: 1, minWidth: '180px' } });
  searchWrap.innerHTML = '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" class="search-wrap__icon"><circle cx="11" cy="11" r="8"/><line x1="21" y1="21" x2="16.65" y2="16.65"/></svg>';
  const searchInput = el('input', {
    type: 'search', class: 'input', placeholder: t('common.searchPlaceholder'),
    value: KnowledgeState.query,
    onInput: debounce((e) => { KnowledgeState.query = e.target.value; renderList(); }, 200)
  });
  searchWrap.appendChild(searchInput);
  toolbar.appendChild(searchWrap);

  const catSelect = el('select', { class: 'select', style: { maxWidth: '200px' } });
  catSelect.appendChild(el('option', { value: '', text: t('common.all') }));
  for (const cat of DATA_KNOWLEDGE_CATEGORIES) {
    const opt = el('option', { value: cat.id, text: i18n.current === 'ar' ? cat.labelAr : cat.labelEn });
    if (cat.id === KnowledgeState.category) opt.setAttribute('selected', '');
    catSelect.appendChild(opt);
  }
  catSelect.addEventListener('change', (e) => { KnowledgeState.category = e.target.value; renderList(); });
  toolbar.appendChild(catSelect);

  page.appendChild(toolbar);

  const listWrap = el('div');
  page.appendChild(listWrap);

  function renderList() {
    listWrap.innerHTML = '';
    const q = KnowledgeState.query.trim().toLowerCase();
    let filtered = DATA_KNOWLEDGE.filter(a => {
      if (KnowledgeState.category && a.category !== KnowledgeState.category) return false;
      if (!q) return true;
      const hay = [a.titleAr, a.titleEn, a.bodyAr, a.bodyEn].join(' ').toLowerCase();
      return hay.includes(q);
    });

    if (!filtered.length) {
      listWrap.appendChild(el('div', { class: 'empty' },
        el('div', { class: 'empty__title', text: t('empty.search') }),
        el('div', { class: 'empty__desc', text: t('empty.searchDesc') })
      ));
      return;
    }

    const bookmarks = getKnowledgeBookmarks();
    const grid = el('div', { class: 'grid grid-2' });

    for (const article of filtered) {
      const card = el('div', { class: 'card' });
      const hdrRow = el('div', { class: 'card-hdr' });
      hdrRow.appendChild(el('div', {
        class: 'card-title',
        text: i18n.current === 'ar' ? article.titleAr : article.titleEn
      }));

      const isBookmarked = bookmarks.includes(article.id);
      hdrRow.appendChild(el('button', {
        type: 'button', class: 'btn btn-ghost btn-sm',
        title: isBookmarked ? t('knowledge.unbookmark') : t('knowledge.bookmark'),
        onClick: () => {
          const list = getKnowledgeBookmarks();
          const idx = list.indexOf(article.id);
          if (idx === -1) list.push(article.id);
          else list.splice(idx, 1);
          saveKnowledgeBookmarks(list);
          renderList();
        },
        style: { color: isBookmarked ? 'var(--warning)' : 'var(--text-2)' }
      }, document.createTextNode(isBookmarked ? '★' : '☆')));
      card.appendChild(hdrRow);

      const cat = DATA_KNOWLEDGE_CATEGORIES.find(c => c.id === article.category);
      if (cat) {
        card.appendChild(el('div', {
          class: 'badge',
          text: i18n.current === 'ar' ? cat.labelAr : cat.labelEn,
          style: { alignSelf: 'flex-start' }
        }));
      }

      card.appendChild(el('div', {
        class: 'card-body',
        text: truncate(i18n.current === 'ar' ? article.bodyAr : article.bodyEn, 180)
      }));

      card.appendChild(el('div', { class: 'card-footer' },
        el('button', {
          type: 'button', class: 'btn btn-sm btn-primary',
          onClick: () => openArticle(article)
        }, document.createTextNode(t('knowledge.readMore')))
      ));

      grid.appendChild(card);
    }

    listWrap.appendChild(grid);
  }

  function openArticle(article) {
    const body = el('div');
    body.appendChild(el('div', {
      class: 'badge',
      text: (DATA_KNOWLEDGE_CATEGORIES.find(c => c.id === article.category) || {}).labelAr || '',
      style: { marginBottom: 'var(--s-3)' }
    }));
    body.appendChild(el('div', {
      style: { whiteSpace: 'pre-wrap', lineHeight: '1.7', fontSize: 'var(--fs-sm)', marginBottom: 'var(--s-3)' },
      text: i18n.current === 'ar' ? article.bodyAr : article.bodyEn
    }));
    body.appendChild(el('div', {
      style: { fontSize: 'var(--fs-xs)', color: 'var(--text-3)', borderTop: '1px solid var(--border)', paddingTop: 'var(--s-2)' },
      text: t('knowledge.source') + ': ' + article.source
    }));

    openModal({
      title: i18n.current === 'ar' ? article.titleAr : article.titleEn,
      content: body,
      actions: [{ label: t('common.close'), onClick: (c) => c() }]
    });
  }

  main.appendChild(page);
  renderList();
}

/* ═══════════════════════════════════════════════════════════════
   26. MODULE — Projects
   ═══════════════════════════════════════════════════════════════ */

const PROJECT_STATUSES = [
  { id: 'planning', key: 'projects.statusPlanning', color: 'info' },
  { id: 'active', key: 'projects.statusActive', color: 'success' },
  { id: 'paused', key: 'projects.statusPaused', color: 'warning' },
  { id: 'done', key: 'projects.statusDone', color: 'success' }
];

const ProjectsState = {
  query: '',
  statusFilter: '',
  sortBy: 'updated'
};

function renderProjects(main) {
  main.innerHTML = '';

  const page = el('div', { class: 'page' });
  const hdr = el('div', { class: 'page-hdr' });
  const hdrMain = el('div', { class: 'page-hdr__main' });
  hdrMain.appendChild(el('h1', { class: 'page-title', text: t('projects.title') }));
  hdrMain.appendChild(el('div', { class: 'page-sub', text: t('projects.syncNote') }));
  hdr.appendChild(hdrMain);
  hdr.appendChild(el('button', {
    type: 'button', class: 'btn btn-primary',
    onClick: () => openProjectEditor(null)
  }, icon('plus', 14), document.createTextNode(' ' + t('projects.new'))));
  page.appendChild(hdr);

  const toolbar = el('div', { class: 'toolbar' });
  const searchWrap = el('div', { class: 'search-wrap', style: { flex: 1, minWidth: '180px' } });
  searchWrap.innerHTML = '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" class="search-wrap__icon"><circle cx="11" cy="11" r="8"/><line x1="21" y1="21" x2="16.65" y2="16.65"/></svg>';
  const searchInput = el('input', {
    type: 'search', class: 'input', placeholder: t('common.searchPlaceholder'),
    value: ProjectsState.query,
    onInput: debounce((e) => { ProjectsState.query = e.target.value; renderList(); }, 200)
  });
  searchWrap.appendChild(searchInput);
  toolbar.appendChild(searchWrap);

  const statusSelect = el('select', { class: 'select', style: { maxWidth: '180px' } });
  statusSelect.appendChild(el('option', { value: '', text: t('common.all') }));
  for (const s of PROJECT_STATUSES) {
    const opt = el('option', { value: s.id, text: t(s.key) });
    if (s.id === ProjectsState.statusFilter) opt.setAttribute('selected', '');
    statusSelect.appendChild(opt);
  }
  statusSelect.addEventListener('change', (e) => { ProjectsState.statusFilter = e.target.value; renderList(); });
  toolbar.appendChild(statusSelect);

  const sortSelect = el('select', { class: 'select', style: { maxWidth: '180px' } });
  sortSelect.appendChild(el('option', { value: 'updated', text: t('scripts.sortUpdated') }));
  sortSelect.appendChild(el('option', { value: 'created', text: t('scripts.sortCreated') }));
  sortSelect.appendChild(el('option', { value: 'title', text: t('common.title') }));
  sortSelect.value = ProjectsState.sortBy;
  sortSelect.addEventListener('change', (e) => { ProjectsState.sortBy = e.target.value; renderList(); });
  toolbar.appendChild(sortSelect);

  page.appendChild(toolbar);

  const listWrap = el('div');
  page.appendChild(listWrap);

  function renderList() {
    listWrap.innerHTML = '';
    let projects = getProjects();

    const q = ProjectsState.query.trim().toLowerCase();
    if (q) {
      projects = projects.filter(p =>
        (p.title || '').toLowerCase().includes(q) ||
        (p.description || '').toLowerCase().includes(q)
      );
    }
    if (ProjectsState.statusFilter) {
      projects = projects.filter(p => p.status === ProjectsState.statusFilter);
    }

    projects.sort((a, b) => {
      if (ProjectsState.sortBy === 'title') return (a.title || '').localeCompare(b.title || '');
      if (ProjectsState.sortBy === 'created') return (b.createdAt || 0) - (a.createdAt || 0);
      return (b.updatedAt || 0) - (a.updatedAt || 0);
    });

    if (!projects.length) {
      const empty = el('div', { class: 'empty' });
      const eicon = icon('folder', 40);
      eicon.setAttribute('class', 'empty__icon');
      empty.appendChild(eicon);
      empty.appendChild(el('div', {
        class: 'empty__title',
        text: q || ProjectsState.statusFilter ? t('empty.search') : t('empty.projects')
      }));
      empty.appendChild(el('div', {
        class: 'empty__desc',
        text: q ? t('empty.searchDesc') : t('empty.projectsDesc')
      }));
      empty.appendChild(el('button', {
        type: 'button', class: 'btn btn-primary',
        onClick: () => openProjectEditor(null)
      }, document.createTextNode(t('projects.new'))));
      listWrap.appendChild(empty);
      return;
    }

    const grid = el('div', { class: 'grid grid-2' });
    for (const project of projects) {
      grid.appendChild(buildProjectCard(project));
    }
    listWrap.appendChild(grid);
  }

  function buildProjectCard(project) {
    const card = el('div', { class: 'card' });

    const hdrRow = el('div', { class: 'card-hdr' });
    hdrRow.appendChild(el('div', { class: 'card-title', text: project.title }));

    const statusDef = PROJECT_STATUSES.find(s => s.id === project.status);
    if (statusDef) {
      hdrRow.appendChild(el('span', {
        class: `badge badge-${statusDef.color}`,
        text: t(statusDef.key)
      }));
    }
    card.appendChild(hdrRow);

    if (project.description) {
      card.appendChild(el('div', { class: 'card-sub', text: truncate(project.description, 160) }));
    }

    const attachedScripts = (project.scriptIds || []).length;
    const meta = el('div', { class: 'row', style: { gap: 'var(--s-2)', flexWrap: 'wrap' } });
    meta.appendChild(el('span', {
      class: 'badge',
      text: `${attachedScripts} ${t('projects.attachScripts')}`
    }));
    if (project.createdAt) {
      meta.appendChild(el('span', {
        class: 'badge',
        text: t('common.created') + ': ' + formatRelative(project.createdAt)
      }));
    }
    card.appendChild(meta);

    if (project.notes) {
      card.appendChild(el('div', {
        style: {
          fontSize: 'var(--fs-xs)', color: 'var(--text-2)',
          borderTop: '1px solid var(--border)',
          paddingTop: 'var(--s-2)'
        },
        text: truncate(project.notes, 140)
      }));
    }

    const footer = el('div', { class: 'card-footer' });
    footer.appendChild(iconBtn('edit', t('common.edit'), () => openProjectEditor(project)));
    footer.appendChild(iconBtn('trash', t('common.delete'), async () => {
      const ok = await confirmDialog({
        title: t('confirm.deleteProject'),
        message: t('common.deleteWarning'),
        danger: true,
        confirmLabel: t('common.delete')
      });
      if (ok) {
        const list = getProjects().filter(p => p.id !== project.id);
        writeList('projects', list);
        const scripts = getScripts().map(s =>
          s.projectId === project.id ? { ...s, projectId: null } : s
        );
        saveScripts(scripts);
        renderList();
        showToast(t('common.deleted'), 'ok', 2000);
      }
    }));
    card.appendChild(footer);

    return card;
  }

  main.appendChild(page);
  renderList();
}

function openProjectEditor(existing) {
  const isEdit = !!existing;
  const project = existing ? { ...existing } : {
    id: uid('p_'),
    title: '',
    description: '',
    status: 'planning',
    scriptIds: [],
    notes: '',
    createdAt: Date.now(),
    updatedAt: Date.now()
  };

  const form = el('div', { class: 'stack' });

  const titleField = el('div', { class: 'field' });
  titleField.appendChild(el('label', { class: 'field__lbl', text: t('common.title') + ' *' }));
  const titleInput = el('input', { type: 'text', class: 'input', value: project.title, maxlength: '100' });
  titleField.appendChild(titleInput);
  form.appendChild(titleField);

  const descField = el('div', { class: 'field' });
  descField.appendChild(el('label', { class: 'field__lbl', text: t('common.description') }));
  const descInput = el('textarea', { class: 'textarea', rows: '2', maxlength: '500' });
  descInput.value = project.description || '';
  descField.appendChild(descInput);
  form.appendChild(descField);

  const statusField = el('div', { class: 'field' });
  statusField.appendChild(el('label', { class: 'field__lbl', text: t('common.status') }));
  const statusSelect = el('select', { class: 'select' });
  for (const s of PROJECT_STATUSES) {
    const opt = el('option', { value: s.id, text: t(s.key) });
    if (s.id === project.status) opt.setAttribute('selected', '');
    statusSelect.appendChild(opt);
  }
  statusField.appendChild(statusSelect);
  form.appendChild(statusField);

  const notesField = el('div', { class: 'field' });
  notesField.appendChild(el('label', { class: 'field__lbl', text: t('projects.notes') }));
  const notesInput = el('textarea', { class: 'textarea', rows: '3' });
  notesInput.value = project.notes || '';
  notesField.appendChild(notesInput);
  form.appendChild(notesField);

  const scriptsAll = getScripts();
  if (scriptsAll.length) {
    const attachField = el('div', { class: 'field' });
    attachField.appendChild(el('label', { class: 'field__lbl', text: t('projects.attachScripts') }));
    const list = el('div', { class: 'stack stack-sm', style: { maxHeight: '180px', overflowY: 'auto', padding: 'var(--s-2)', border: '1px solid var(--border)', borderRadius: 'var(--r-md)' } });
    const checks = [];
    for (const s of scriptsAll) {
      const label = el('label', { class: 'checkbox' });
      const cb = el('input', { type: 'checkbox' });
      cb.checked = (project.scriptIds || []).includes(s.id);
      cb.dataset.scriptId = s.id;
      checks.push(cb);
      label.appendChild(cb);
      label.appendChild(el('span', { text: `${s.title} (${getLangLabel(s.language)})`, style: { fontSize: 'var(--fs-sm)' } }));
      list.appendChild(label);
    }
    attachField.appendChild(list);
    form.appendChild(attachField);
    project._checks = checks;
  }

  openModal({
    title: isEdit ? t('common.edit') : t('projects.new'),
    content: form,
    actions: [
      { label: t('common.cancel'), onClick: (c) => c() },
      {
        label: t('common.save'),
        class: 'btn-primary',
        onClick: (c) => {
          const title = titleInput.value.trim();
          if (!title) {
            titleInput.classList.add('input-error');
            titleInput.focus();
            return;
          }
          project.title = title;
          project.description = descInput.value.trim();
          project.status = statusSelect.value;
          project.notes = notesInput.value.trim();
          project.updatedAt = Date.now();
          if (project._checks) {
            project.scriptIds = project._checks.filter(cb => cb.checked).map(cb => cb.dataset.scriptId);
            delete project._checks;
          }

          const list = getProjects();
          const idx = list.findIndex(p => p.id === project.id);
          if (idx === -1) list.unshift(project);
          else list[idx] = project;
          writeList('projects', list);

          const scriptsAll = getScripts();
          for (const s of scriptsAll) {
            const shouldAttach = (project.scriptIds || []).includes(s.id);
            if (shouldAttach && s.projectId !== project.id) {
              s.projectId = project.id;
            } else if (!shouldAttach && s.projectId === project.id) {
              s.projectId = null;
            }
          }
          saveScripts(scriptsAll);

          c();
          Router.refresh();
          showToast(isEdit ? t('common.updated_ok') : t('common.created_ok'), 'ok', 2000);
        }
      }
    ]
  });

  setTimeout(() => titleInput.focus(), 80);
}

/* ═══════════════════════════════════════════════════════════════
   27. MODULE — Security Reports
   ═══════════════════════════════════════════════════════════════ */

const SEVERITIES = [
  { id: 'info', key: 'sev.info', class: 'sev-info' },
  { id: 'low', key: 'sev.low', class: 'sev-low' },
  { id: 'med', key: 'sev.med', class: 'sev-med' },
  { id: 'high', key: 'sev.high', class: 'sev-high' },
  { id: 'crit', key: 'sev.crit', class: 'sev-crit' }
];

const ReportsState = {
  query: '',
  sortBy: 'updated'
};

function renderReports(main) {
  main.innerHTML = '';

  const page = el('div', { class: 'page' });
  const hdr = el('div', { class: 'page-hdr' });
  const hdrMain = el('div', { class: 'page-hdr__main' });
  hdrMain.appendChild(el('h1', { class: 'page-title', text: t('reports.title') }));
  hdr.appendChild(hdrMain);
  hdr.appendChild(el('button', {
    type: 'button', class: 'btn btn-primary',
    onClick: () => openReportEditor(null)
  }, icon('plus', 14), document.createTextNode(' ' + t('reports.new'))));
  page.appendChild(hdr);

  const disclaimer = el('div', { class: 'banner banner-warn' });
  disclaimer.innerHTML = TOAST_ICONS.warn;
  disclaimer.appendChild(el('div', { text: t('reports.disclaimer'), style: { fontSize: 'var(--fs-sm)' } }));
  page.appendChild(disclaimer);

  const toolbar = el('div', { class: 'toolbar' });
  const searchWrap = el('div', { class: 'search-wrap', style: { flex: 1, minWidth: '180px' } });
  searchWrap.innerHTML = '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" class="search-wrap__icon"><circle cx="11" cy="11" r="8"/><line x1="21" y1="21" x2="16.65" y2="16.65"/></svg>';
  const searchInput = el('input', {
    type: 'search', class: 'input', placeholder: t('common.searchPlaceholder'),
    value: ReportsState.query,
    onInput: debounce((e) => { ReportsState.query = e.target.value; renderList(); }, 200)
  });
  searchWrap.appendChild(searchInput);
  toolbar.appendChild(searchWrap);

  const sortSelect = el('select', { class: 'select', style: { maxWidth: '180px' } });
  sortSelect.appendChild(el('option', { value: 'updated', text: t('scripts.sortUpdated') }));
  sortSelect.appendChild(el('option', { value: 'created', text: t('scripts.sortCreated') }));
  sortSelect.appendChild(el('option', { value: 'title', text: t('common.title') }));
  sortSelect.value = ReportsState.sortBy;
  sortSelect.addEventListener('change', (e) => { ReportsState.sortBy = e.target.value; renderList(); });
  toolbar.appendChild(sortSelect);
  page.appendChild(toolbar);

  const listWrap = el('div');
  page.appendChild(listWrap);

  function renderList() {
    listWrap.innerHTML = '';
    let reports = readList('reports');

    const q = ReportsState.query.trim().toLowerCase();
    if (q) {
      reports = reports.filter(r =>
        (r.title || '').toLowerCase().includes(q) ||
        (r.execSummary || '').toLowerCase().includes(q)
      );
    }

    reports.sort((a, b) => {
      if (ReportsState.sortBy === 'title') return (a.title || '').localeCompare(b.title || '');
      if (ReportsState.sortBy === 'created') return (b.createdAt || 0) - (a.createdAt || 0);
      return (b.updatedAt || 0) - (a.updatedAt || 0);
    });

    if (!reports.length) {
      const empty = el('div', { class: 'empty' });
      const eicon = icon('file', 40);
      eicon.setAttribute('class', 'empty__icon');
      empty.appendChild(eicon);
      empty.appendChild(el('div', {
        class: 'empty__title',
        text: q ? t('empty.search') : t('empty.reports')
      }));
      empty.appendChild(el('div', {
        class: 'empty__desc',
        text: q ? t('empty.searchDesc') : t('empty.reportsDesc')
      }));
      empty.appendChild(el('button', {
        type: 'button', class: 'btn btn-primary',
        onClick: () => openReportEditor(null)
      }, document.createTextNode(t('reports.new'))));
      listWrap.appendChild(empty);
      return;
    }

    const stack = el('div', { class: 'stack' });
    for (const report of reports) {
      stack.appendChild(buildReportItem(report));
    }
    listWrap.appendChild(stack);
  }

  function buildReportItem(report) {
    const item = el('div', { class: 'list-item' });
    const mainEl = el('div', { class: 'list-item__main' });

    const titleRow = el('div', { class: 'list-item__title' });
    titleRow.appendChild(el('span', { text: report.title }));
    const findingsCount = (report.findings || []).length;
    if (findingsCount) {
      const maxSev = (report.findings || []).reduce((max, f) => {
        const order = ['info', 'low', 'med', 'high', 'crit'];
        return order.indexOf(f.severity) > order.indexOf(max) ? f.severity : max;
      }, 'info');
      const sevDef = SEVERITIES.find(s => s.id === maxSev);
      if (sevDef) {
        titleRow.appendChild(el('span', { class: `sev ${sevDef.class}`, text: t(sevDef.key) }));
      }
      titleRow.appendChild(el('span', { class: 'badge', text: `${findingsCount}` }));
    }
    mainEl.appendChild(titleRow);

    if (report.execSummary) {
      mainEl.appendChild(el('div', { class: 'list-item__sub', text: truncate(report.execSummary, 140) }));
    }

    mainEl.appendChild(el('div', {
      class: 'list-item__sub',
      style: { color: 'var(--text-3)', fontSize: 'var(--fs-xs)' },
      text: formatRelative(report.updatedAt || report.createdAt)
    }));

    item.appendChild(mainEl);

    const actions = el('div', { class: 'list-item__actions' });
    actions.appendChild(iconBtn('edit', t('common.edit'), () => openReportEditor(report)));
    actions.appendChild(iconBtn('download', t('reports.exportTxt'), () => exportReportTxt(report)));
    actions.appendChild(iconBtn('copy', t('reports.exportJson'), () => exportReportJson(report)));
    actions.appendChild(iconBtn('trash', t('common.delete'), async () => {
      const ok = await confirmDialog({
        title: t('confirm.deleteReport'),
        message: t('common.deleteWarning'),
        danger: true,
        confirmLabel: t('common.delete')
      });
      if (ok) {
        const list = readList('reports').filter(r => r.id !== report.id);
        writeList('reports', list);
        renderList();
        showToast(t('common.deleted'), 'ok', 2000);
      }
    }));
    item.appendChild(actions);

    return item;
  }

  main.appendChild(page);
  renderList();
}

function exportReportTxt(report) {
  const lines = [];
  lines.push(`# ${report.title}`);
  lines.push(`Generated: ${new Date().toISOString()}`);
  lines.push('');
  if (report.scope) {
    lines.push(`## ${t('reports.scope')}`);
    lines.push(report.scope);
    lines.push('');
  }
  if (report.execSummary) {
    lines.push(`## ${t('reports.execSummary')}`);
    lines.push(report.execSummary);
    lines.push('');
  }
  if ((report.findings || []).length) {
    lines.push(`## ${t('reports.findings')}`);
    for (let i = 0; i < report.findings.length; i++) {
      const f = report.findings[i];
      const sev = SEVERITIES.find(s => s.id === f.severity);
      lines.push(`### ${i + 1}. ${f.title || '(untitled)'} [${sev ? t(sev.key) : f.severity}]`);
      if (f.source) lines.push(`Source: ${f.source}`);
      if (f.evidence) { lines.push(`Evidence:`); lines.push(f.evidence); }
      if (f.recommendation) { lines.push(`Recommendation:`); lines.push(f.recommendation); }
      lines.push('');
    }
  }
  if (report.references) {
    lines.push(`## ${t('reports.references')}`);
    lines.push(report.references);
    lines.push('');
  }
  lines.push('---');
  lines.push('Manual report — no automated scans performed.');

  const ok = download(`nexsec-report-${sanitizeFilename(report.title || 'report')}.txt`, lines.join('\n'));
  if (ok) showToast(t('common.saved'), 'ok', 2000);
}

function exportReportJson(report) {
  const clean = { ...report };
  delete clean._checks;
  const ok = download(
    `nexsec-report-${sanitizeFilename(report.title || 'report')}.json`,
    JSON.stringify(clean, null, 2),
    'application/json;charset=utf-8'
  );
  if (ok) showToast(t('common.saved'), 'ok', 2000);
}

function openReportEditor(existing) {
  const isEdit = !!existing;
  const report = existing ? JSON.parse(JSON.stringify(existing)) : {
    id: uid('r_'),
    title: '',
    scope: '',
    execSummary: '',
    findings: [],
    references: '',
    createdAt: Date.now(),
    updatedAt: Date.now()
  };

  const form = el('div', { class: 'stack' });

  const titleField = el('div', { class: 'field' });
  titleField.appendChild(el('label', { class: 'field__lbl', text: t('common.title') + ' *' }));
  const titleInput = el('input', { type: 'text', class: 'input', value: report.title, maxlength: '150' });
  titleField.appendChild(titleInput);
  form.appendChild(titleField);

  const scopeField = el('div', { class: 'field' });
  scopeField.appendChild(el('label', { class: 'field__lbl', text: t('reports.scope') }));
  const scopeInput = el('textarea', { class: 'textarea', rows: '2' });
  scopeInput.value = report.scope || '';
  scopeField.appendChild(scopeInput);
  form.appendChild(scopeField);

  const summaryField = el('div', { class: 'field' });
  summaryField.appendChild(el('label', { class: 'field__lbl', text: t('reports.execSummary') }));
  const summaryInput = el('textarea', { class: 'textarea', rows: '3' });
  summaryInput.value = report.execSummary || '';
  summaryField.appendChild(summaryInput);
  form.appendChild(summaryField);

  const findingsWrap = el('div', { class: 'stack stack-sm' });
  findingsWrap.appendChild(el('div', { class: 'field__lbl', text: t('reports.findings') }));

  function renderFindings() {
    while (findingsWrap.children.length > 1) findingsWrap.removeChild(findingsWrap.lastChild);

    if (!report.findings.length) {
      findingsWrap.appendChild(el('div', {
        class: 'card-sub',
        text: i18n.current === 'ar' ? 'لا توجد نتائج بعد.' : 'No findings yet.'
      }));
    }

    for (let i = 0; i < report.findings.length; i++) {
      const f = report.findings[i];
      const box = el('div', { style: { padding: 'var(--s-2)', border: '1px solid var(--border)', borderRadius: 'var(--r-md)', background: 'var(--bg-1)' } });
      const row1 = el('div', { class: 'row' });
      const fTitle = el('input', {
        type: 'text', class: 'input', value: f.title || '',
        placeholder: t('common.title'),
        style: { flex: 1, minWidth: '140px' },
        onInput: (e) => { report.findings[i].title = e.target.value; }
      });
      row1.appendChild(fTitle);

      const sevSelect = el('select', { class: 'select', style: { maxWidth: '150px' } });
      for (const sv of SEVERITIES) {
        const opt = el('option', { value: sv.id, text: t(sv.key) });
        if (sv.id === f.severity) opt.setAttribute('selected', '');
        sevSelect.appendChild(opt);
      }
      sevSelect.addEventListener('change', (e) => { report.findings[i].severity = e.target.value; });
      row1.appendChild(sevSelect);

      row1.appendChild(iconBtn('trash', t('common.delete'), () => {
        report.findings.splice(i, 1);
        renderFindings();
      }));
      box.appendChild(row1);

      const sourceInput = el('input', {
        type: 'text', class: 'input', value: f.source || '',
        placeholder: (i18n.current === 'ar' ? 'المصدر (يدوي)' : 'Source (manual)'),
        style: { marginTop: 'var(--s-2)' },
        onInput: (e) => { report.findings[i].source = e.target.value; }
      });
      box.appendChild(sourceInput);

      const ev = el('textarea', {
        class: 'textarea', rows: '2', placeholder: t('reports.evidence'),
        style: { marginTop: 'var(--s-2)' }
      });
      ev.value = f.evidence || '';
      ev.addEventListener('input', (e) => { report.findings[i].evidence = e.target.value; });
      box.appendChild(ev);

      const rec = el('textarea', {
        class: 'textarea', rows: '2', placeholder: t('reports.recommendations'),
        style: { marginTop: 'var(--s-2)' }
      });
      rec.value = f.recommendation || '';
      rec.addEventListener('input', (e) => { report.findings[i].recommendation = e.target.value; });
      box.appendChild(rec);

      findingsWrap.appendChild(box);
    }

    findingsWrap.appendChild(el('button', {
      type: 'button', class: 'btn btn-sm',
      onClick: () => {
        report.findings.push({ title: '', severity: 'info', source: '', evidence: '', recommendation: '' });
        renderFindings();
      }
    }, icon('plus', 12), document.createTextNode(' ' + t('reports.addFinding'))));
  }
  renderFindings();
  form.appendChild(findingsWrap);

  const refField = el('div', { class: 'field' });
  refField.appendChild(el('label', { class: 'field__lbl', text: t('reports.references') }));
  const refInput = el('textarea', { class: 'textarea', rows: '2' });
  refInput.value = report.references || '';
  refField.appendChild(refInput);
  form.appendChild(refField);

  openModal({
    title: isEdit ? t('common.edit') : t('reports.new'),
    content: form,
    actions: [
      { label: t('common.cancel'), onClick: (c) => c() },
      {
        label: t('common.save'),
        class: 'btn-primary',
        onClick: (c) => {
          const title = titleInput.value.trim();
          if (!title) {
            titleInput.classList.add('input-error');
            titleInput.focus();
            return;
          }
          report.title = title;
          report.scope = scopeInput.value.trim();
          report.execSummary = summaryInput.value.trim();
          report.references = refInput.value.trim();
          report.updatedAt = Date.now();

          const list = readList('reports');
          const idx = list.findIndex(r => r.id === report.id);
          if (idx === -1) list.unshift(report);
          else list[idx] = report;
          writeList('reports', list);

          c();
          Router.refresh();
          showToast(isEdit ? t('common.updated_ok') : t('common.created_ok'), 'ok', 2000);
        }
      }
    ]
  });

  setTimeout(() => titleInput.focus(), 80);
}

/* ═══════════════════════════════════════════════════════════════
   28. MODULE — Settings
   ═══════════════════════════════════════════════════════════════ */

function renderSettings(main) {
  main.innerHTML = '';
  const current = loadSettings();

  const page = el('div', { class: 'page' });
  const hdr = el('div', { class: 'page-hdr' });
  const hdrMain = el('div', { class: 'page-hdr__main' });
  hdrMain.appendChild(el('h1', { class: 'page-title', text: t('settings.title') }));
  hdr.appendChild(hdrMain);
  page.appendChild(hdr);

  // Language
  const langCard = el('div', { class: 'card' });
  langCard.appendChild(el('div', { class: 'card-title', text: t('settings.language') }));
  langCard.appendChild(el('div', { class: 'card-sub', text: t('settings.languageDesc') }));
  const langRow = el('div', { class: 'row' });
  ['ar', 'en'].forEach(lang => {
    langRow.appendChild(el('button', {
      type: 'button',
      class: 'btn' + (current.lang === lang ? ' btn-primary' : ''),
      onClick: async () => {
        await i18n.setLang(lang);
        Router.refresh();
      },
      text: lang === 'ar' ? 'العربية' : 'English'
    }));
  });
  langCard.appendChild(langRow);
  page.appendChild(langCard);

  // Theme
  const themeCard = el('div', { class: 'card' });
  themeCard.appendChild(el('div', { class: 'card-title', text: t('settings.theme') }));
  themeCard.appendChild(el('div', { class: 'card-sub', text: t('settings.themeDesc') }));
  const themeRow = el('div', { class: 'row' });
  [['dark', t('settings.themeDark')], ['light', t('settings.themeLight')]].forEach(([theme, label]) => {
    themeRow.appendChild(el('button', {
      type: 'button',
      class: 'btn' + (current.theme === theme ? ' btn-primary' : ''),
      onClick: () => {
        saveSettings({ theme });
        applySettingsToDOM();
        Router.refresh();
      },
      text: label
    }));
  });
  themeCard.appendChild(themeRow);
  page.appendChild(themeCard);

  // Font size
  const fontCard = el('div', { class: 'card' });
  fontCard.appendChild(el('div', { class: 'card-title', text: t('settings.fontSize') }));
  fontCard.appendChild(el('div', { class: 'card-sub', text: t('settings.fontSizeDesc') }));
  const fontRow = el('div', { class: 'row' });
  [['sm', t('settings.fontSm')], ['md', t('settings.fontMd')], ['lg', t('settings.fontLg')]].forEach(([size, label]) => {
    fontRow.appendChild(el('button', {
      type: 'button',
      class: 'btn' + (current.fontSize === size ? ' btn-primary' : ''),
      onClick: () => {
        saveSettings({ fontSize: size });
        applySettingsToDOM();
        Router.refresh();
      },
      text: label
    }));
  });
  fontCard.appendChild(fontRow);
  page.appendChild(fontCard);

  // Reduce motion
  const motionCard = el('div', { class: 'card' });
  motionCard.appendChild(el('div', { class: 'card-title', text: t('settings.reduceMotion') }));
  motionCard.appendChild(el('div', { class: 'card-sub', text: t('settings.reduceMotionDesc') }));
  const motionLabel = el('label', { class: 'checkbox', style: { marginTop: 'var(--s-2)' } });
  const motionCb = el('input', { type: 'checkbox' });
  motionCb.checked = !!current.reduceMotion;
  motionCb.addEventListener('change', () => {
    saveSettings({ reduceMotion: motionCb.checked });
    applySettingsToDOM();
  });
  motionLabel.appendChild(motionCb);
  motionLabel.appendChild(el('span', { text: t('common.on') + ' / ' + t('common.off') }));
  motionCard.appendChild(motionLabel);
  page.appendChild(motionCard);

  // Status
  const statusCard = el('div', { class: 'card' });
  statusCard.appendChild(el('div', { class: 'card-title', text: t('settings.status') }));
  const statusList = el('div', { class: 'stack stack-sm' });
  statusList.appendChild(buildStatusRow('status.ai', 'off', t('status.aiLong')));
  statusList.appendChild(buildStatusRow('status.repo', 'off', t('status.repoLong')));
  statusList.appendChild(buildStatusRow('status.backend', 'off', t('status.backendLong')));
  statusList.appendChild(buildStatusRow(null, 'on', Storage.available()
    ? (i18n.current === 'ar' ? 'التخزين المحلي متاح' : 'Local storage available')
    : t('error.storageUnavailable')));
  statusCard.appendChild(statusList);
  page.appendChild(statusCard);

  // Privacy
  const privacyCard = el('div', { class: 'card' });
  privacyCard.appendChild(el('div', { class: 'card-title', text: t('settings.privacy') }));
  privacyCard.appendChild(el('div', { class: 'card-sub', text: t('settings.privacyDesc') }));
  page.appendChild(privacyCard);

  // Data export/import
  const dataCard = el('div', { class: 'card' });
  dataCard.appendChild(el('div', { class: 'card-title', text: t('settings.export') + ' / ' + t('settings.import') }));
  dataCard.appendChild(el('div', { class: 'card-sub', text: t('settings.exportDesc') }));

  const dataRow = el('div', { class: 'row' });
  dataRow.appendChild(el('button', {
    type: 'button', class: 'btn',
    onClick: () => {
      const dump = Storage.exportAll();
      const ok = download(
        `nexsec-backup-${new Date().toISOString().slice(0, 10)}.json`,
        JSON.stringify(dump, null, 2),
        'application/json;charset=utf-8'
      );
      if (ok) showToast(t('common.saved'), 'ok', 2500);
    }
  }, icon('download', 14), document.createTextNode(' ' + t('settings.export'))));

  const fileInput = el('input', { type: 'file', accept: '.json,application/json', style: { display: 'none' } });
  fileInput.addEventListener('change', async (e) => {
    const file = e.target.files?.[0];
    if (!file) return;
    const ok = await confirmDialog({
      title: t('settings.import'),
      message: t('settings.importDesc'),
      danger: true,
      confirmLabel: t('common.confirm')
    });
    if (!ok) { fileInput.value = ''; return; }
    const reader = new FileReader();
    reader.onload = () => {
      try {
        const parsed = safeJSON(reader.result, null);
        const count = Storage.importAll(parsed, { merge: false });
        showToast(`${t('common.saved')} (${count})`, 'ok', 3000);
        Router.refresh();
      } catch {
        showToast(t('error.invalidFile'), 'err', 3500);
      }
    };
    reader.onerror = () => showToast(t('error.generic'), 'err', 3500);
    reader.readAsText(file, 'utf-8');
    fileInput.value = '';
  });
  dataRow.appendChild(fileInput);
  dataRow.appendChild(el('button', {
    type: 'button', class: 'btn',
    onClick: () => fileInput.click()
  }, icon('copy', 14), document.createTextNode(' ' + t('settings.import'))));
  dataCard.appendChild(dataRow);
  page.appendChild(dataCard);

  // Danger zone
  const danger = el('div', { class: 'danger-zone' });
  danger.appendChild(el('div', { style: { fontWeight: 600, marginBottom: 'var(--s-2)' }, text: t('common.warning') }));

  danger.appendChild(el('button', {
    type: 'button', class: 'btn btn-danger',
    style: { marginTop: 'var(--s-2)' },
    onClick: async () => {
      const ok = await confirmDialog({
        title: t('settings.clearData'),
        message: t('settings.clearDataConfirm'),
        danger: true,
        confirmLabel: t('settings.clearData')
      });
      if (ok) {
        Storage.clearAll();
        showToast(t('common.deleted'), 'ok', 2500);
        Router.refresh();
      }
    }
  }, document.createTextNode(t('settings.clearData'))));

  danger.appendChild(el('button', {
    type: 'button', class: 'btn',
    style: { marginTop: 'var(--s-2)' },
    onClick: async () => {
      const ok = await confirmDialog({
        title: t('settings.reset'),
        message: t('settings.resetConfirm'),
        confirmLabel: t('common.confirm')
      });
      if (ok) {
        resetSettings();
        Router.refresh();
        showToast(t('common.saved'), 'ok', 2000);
      }
    }
  }, document.createTextNode(t('settings.reset'))));

  page.appendChild(danger);

  const versionRow = el('div', { class: 'row', style: { color: 'var(--text-3)', fontSize: 'var(--fs-xs)', justifyContent: 'center', paddingTop: 'var(--s-4)' } });
  versionRow.textContent = `NexSec AI — ${t('app.version')}`;
  page.appendChild(versionRow);

  main.appendChild(page);
}

function buildStatusRow(labelKey, state, desc) {
  const row = el('div', { class: 'list-item', style: { padding: 'var(--s-2) var(--s-3)' } });
  const mainEl = el('div', { class: 'list-item__main' });
  const titleRow = el('div', { class: 'list-item__title' });
  const dot = el('span', { class: `status-dot status-${state}`, style: { marginInlineEnd: '6px' } });
  titleRow.appendChild(dot);
  titleRow.appendChild(el('span', { text: labelKey ? t(labelKey) : desc }));
  mainEl.appendChild(titleRow);
  if (labelKey && desc) {
    mainEl.appendChild(el('div', { class: 'list-item__sub', text: desc }));
  }
  row.appendChild(mainEl);
  return row;
}

/* ═══════════════════════════════════════════════════════════════
   29. MODULE — About
   ═══════════════════════════════════════════════════════════════ */

function renderAbout(main) {
  main.innerHTML = '';

  const page = el('div', { class: 'page' });
  const hdr = el('div', { class: 'page-hdr' });
  const hdrMain = el('div', { class: 'page-hdr__main' });
  hdrMain.appendChild(el('h1', { class: 'page-title', text: t('about.title') }));
  hdrMain.appendChild(el('div', { class: 'page-sub', text: t('about.tagline') }));
  hdr.appendChild(hdrMain);
  page.appendChild(hdr);

  const hero = el('div', { class: 'hero' });
  const heroLogo = document.createElementNS('http://www.w3.org/2000/svg', 'svg');
  heroLogo.setAttribute('viewBox', '0 0 64 64');
  heroLogo.setAttribute('class', 'hero__logo');
  heroLogo.innerHTML = `
    <rect width="64" height="64" rx="14" fill="#0a0e12"/>
    <path d="M32 8 L52 16 L52 32 C52 44 42 54 32 58 C22 54 12 44 12 32 L12 16 Z" fill="none" stroke="#10b981" stroke-width="2.5" stroke-linejoin="round"/>
    <polygon points="32,20 42,25.5 42,37 32,42.5 22,37 22,25.5" fill="none" stroke="#34d399" stroke-width="1.8" stroke-linejoin="round"/>
    <circle cx="32" cy="31.5" r="3" fill="#34d399"/>
  `;
  hero.appendChild(heroLogo);

  const heroBody = el('div', { class: 'hero__body' });
  heroBody.appendChild(el('div', { class: 'hero__title', text: 'NexSec AI' }));
  heroBody.appendChild(el('div', { class: 'hero__sub', text: t('about.description') }));
  const badges = el('div', { class: 'row', style: { marginTop: 'var(--s-2)' } });
  badges.appendChild(el('span', { class: 'badge', text: t('about.version') + ': 1.0' }));
  badges.appendChild(el('span', { class: 'badge', text: t('about.license') }));
  heroBody.appendChild(badges);
  hero.appendChild(heroBody);
  page.appendChild(hero);

  const limCard = el('div', { class: 'card' });
  limCard.appendChild(el('div', { class: 'card-title', text: t('about.limitations') }));
  limCard.appendChild(el('div', { class: 'card-sub', text: t('about.limitationsDesc') }));

  const limList = el('div', { class: 'stack stack-sm', style: { marginTop: 'var(--s-2)' } });
  const limitations = i18n.current === 'ar' ? [
    'الذكاء الاصطناعي غير متصل — لا ردود من نموذج AI.',
    'البحث المباشر في المستودعات معطّل — يفتح بحث GitHub الرسمي فقط.',
    'التحليل التلقائي للكود غير متاح — قائمة تحقق يدوية فقط.',
    'لا يتم تنفيذ أي كود أو سكربت في التطبيق.',
    'لا مسح أمني آلي — النتائج والتقارير يدوية 100%.',
    'لا يوجد خادم خلفي — كل شيء يعمل في المتصفح.',
    'البيانات محلية فقط — لا مزامنة بين الأجهزة.'
  ] : [
    'AI is not connected — no model responses.',
    'Live repository search disabled — opens GitHub only.',
    'Automated code analysis unavailable — manual checklist only.',
    'No code or script is executed in the app.',
    'No automated security scans — 100% manual findings.',
    'No backend — everything runs in the browser.',
    'Local data only — no cross-device sync.'
  ];
  for (const lim of limitations) {
    const row = el('div', { class: 'row', style: { gap: 'var(--s-2)', alignItems: 'flex-start' } });
    row.appendChild(el('span', { text: '•', style: { color: 'var(--warning)' } }));
    row.appendChild(el('span', { text: lim, style: { fontSize: 'var(--fs-sm)' } }));
    limList.appendChild(row);
  }
  limCard.appendChild(limList);
  page.appendChild(limCard);

  const privCard = el('div', { class: 'card' });
  privCard.appendChild(el('div', { class: 'card-title', text: t('about.privacy') }));
  privCard.appendChild(el('div', { class: 'card-sub', text: t('about.privacyDesc') }));
  page.appendChild(privCard);

  const statsCard = el('div', { class: 'card' });
  statsCard.appendChild(el('div', { class: 'card-title', text: i18n.current === 'ar' ? 'إحصائيات محلية' : 'Local Stats' }));
  const stats = el('div', { class: 'grid grid-4', style: { marginTop: 'var(--s-2)' } });
  const statDefs = [
    { val: getProjects().length, lbl: t('dashboard.projects') },
    { val: getScripts().length, lbl: t('dashboard.scripts') },
    { val: readList('reports').length, lbl: t('dashboard.reports') },
    { val: getConversations().length, lbl: t('dashboard.chats') }
  ];
  for (const s of statDefs) {
    const cell = el('div', { class: 'card', style: { padding: 'var(--s-3)' } });
    cell.appendChild(el('div', { class: 'stat__val', text: String(s.val) }));
    cell.appendChild(el('div', { class: 'stat__lbl', text: s.lbl }));
    stats.appendChild(cell);
  }
  statsCard.appendChild(stats);
  page.appendChild(statsCard);

  main.appendChild(page);
}

/* ═══════════════════════════════════════════════════════════════
   30. MODULE — 404
   ═══════════════════════════════════════════════════════════════ */

function renderNotFound(main) {
  main.innerHTML = '';
  const page = el('div', { class: 'page' });
  const empty = el('div', { class: 'empty' });
  const iconSvg = icon('alert', 48);
  iconSvg.setAttribute('class', 'empty__icon');
  empty.appendChild(iconSvg);
  empty.appendChild(el('div', { class: 'empty__title', text: t('error.notFound') }));
  empty.appendChild(el('div', { class: 'empty__desc', text: t('error.notFoundDesc') }));
  empty.appendChild(el('button', {
    type: 'button', class: 'btn btn-primary',
    onClick: () => Router.navigate('dashboard')
  }, document.createTextNode(t('nav.dashboard'))));
  page.appendChild(empty);
  main.appendChild(page);
}

/* ═══════════════════════════════════════════════════════════════
   ROUTER REGISTRATION
   ═══════════════════════════════════════════════════════════════ */

Router.register('dashboard', renderDashboard);
Router.register('chat', renderChat);
Router.register('code-studio', renderCodeStudio);
Router.register('repositories', renderRepositorySearch);
Router.register('scripts', renderScriptLibrary);
Router.register('tools', renderTools);
Router.register('knowledge', renderKnowledge);
Router.register('projects', renderProjects);
Router.register('reports', renderReports);
Router.register('settings', renderSettings);
Router.register('about', renderAbout);
Router.register('404', renderNotFound);

/* ═══════════════════════════════════════════════════════════════
   31. BOOTSTRAP
   ═══════════════════════════════════════════════════════════════ */

function bootstrap() {
  const settings = loadSettings();
  applySettingsToDOM(settings);
  i18n.current = settings.lang || 'ar';
  document.documentElement.lang = i18n.current;
  document.documentElement.dir = i18n.current === 'ar' ? 'rtl' : 'ltr';

  const langLabel = $('#langLabel');
  if (langLabel) langLabel.textContent = i18n.current === 'ar' ? 'EN' : 'AR';

  i18n.applyToDOM();
  initShellEvents();

  if (!Storage.available()) {
    showToast(t('error.storageUnavailable'), 'warn', 6000);
  }

  Router.start();

  State.on('lang:changed', () => {});

  try {
    console.log(
      '%cNexSec AI v1.0%c — Frontend-First\nAI: Not Connected · No backend · Local only',
      'background:#10b981;color:#07110c;padding:4px 8px;border-radius:4px;font-weight:bold',
      'color:#8b97a5'
    );
  } catch {}
}

if (document.readyState === 'loading') {
  document.addEventListener('DOMContentLoaded', bootstrap);
} else {
  bootstrap();
}
</script>
</body>
</html>
