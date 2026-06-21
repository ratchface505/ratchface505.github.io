# ratchface505.github.io
who knows

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
<meta name="apple-mobile-web-app-title" content="Jacked Summer">
<title>Jacked Summer 2026</title>
<style>
*{box-sizing:border-box;margin:0;padding:0}
:root{
  --gold:#c8a96e;--gold-dim:#a8893e;--gold-bg:rgba(200,169,110,0.10);
  --bg:#111;--bg2:#1a1a1a;--bg3:#222;
  --border:#2a2a2a;--border2:#333;
  --text:#f0f0f0;--text2:#aaa;--text3:#666;
  --red:#e05555;--green:#4caf7d;--blue:#4a9eff;
  --title:#f0f0f0;
}
.lm{
  --bg:#f0efe9;--bg2:#fff;--bg3:#e8e7e1;
  --border:#d8d7d0;--border2:#ccc;
  --text:#111;--text2:#555;--text3:#888;
  --title:#111;
}
body{font-family:-apple-system,BlinkMacSystemFont,'SF Pro Text',system-ui,sans-serif;background:var(--bg);color:var(--text);font-size:14px;-webkit-tap-highlight-color:transparent}
.app{max-width:430px;margin:0 auto;min-height:100svh;display:flex;flex-direction:column;padding-bottom:env(safe-area-inset-bottom)}

/* HEADER */
.hdr{padding:14px 16px 12px;border-bottom:0.5px solid var(--border);padding-top:calc(14px + env(safe-area-inset-top))}
.hdr-top{display:flex;align-items:flex-start;justify-content:space-between;margin-bottom:10px}
.logo-main{font-size:17px;font-weight:700;letter-spacing:.1em;color:var(--title)}
.mode-btn{background:none;border:0.5px solid var(--border2);border-radius:6px;color:var(--text2);padding:5px 8px;cursor:pointer;font-size:13px;flex-shrink:0}

/* PROGRESS ROW */
.prog-row{display:flex;align-items:center;gap:7px}
.week-chip{font-size:10px;letter-spacing:.1em;color:var(--text3);background:var(--bg3);border:0.5px solid var(--border);border-radius:4px;padding:3px 8px;white-space:nowrap}
.deload-chip{font-size:10px;letter-spacing:.08em;color:#7a3d00;background:#fdf0dc;border:0.5px solid var(--gold);border-radius:4px;padding:3px 8px;white-space:nowrap}
.sess-dots{display:flex;gap:4px;flex-shrink:0}
.sdot{width:22px;height:22px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:9px;font-weight:700;border:1.5px solid var(--border2);background:var(--bg3);color:var(--text3)}
.sdot.done{border-color:var(--green);color:var(--green);background:rgba(76,175,125,0.12)}
.sdot.next{border-color:var(--blue);color:var(--blue);background:rgba(74,158,255,0.12)}
.prog-bar-bg{flex:1;height:3px;background:var(--bg3);border-radius:2px;overflow:hidden;min-width:20px}
.prog-bar-fill{height:3px;background:var(--gold);border-radius:2px;transition:width .6s}
.prog-label{font-size:9px;color:var(--text3);white-space:nowrap}

/* NAV */
.nav{display:flex;border-bottom:0.5px solid var(--border);overflow-x:auto;-webkit-overflow-scrolling:touch}
.nav::-webkit-scrollbar{display:none}
.nav button{flex:1;min-width:52px;background:none;border:none;color:var(--text3);font-size:10px;letter-spacing:.07em;padding:10px 3px;cursor:pointer;border-bottom:2px solid transparent;white-space:nowrap}
.nav button.active{color:var(--gold);border-bottom-color:var(--gold)}
.content{flex:1;padding:14px 16px;overflow-y:auto;-webkit-overflow-scrolling:touch}
.sec-label{font-size:9px;letter-spacing:.14em;color:var(--text3);margin-bottom:10px}
.card{background:var(--bg2);border:0.5px solid var(--border);border-radius:10px;padding:12px 14px;margin-bottom:10px}

/* HOME */
.today-session{background:var(--bg2);border:0.5px solid var(--border);border-radius:12px;padding:18px;margin-bottom:14px}
.today-label{font-size:9px;letter-spacing:.14em;color:var(--gold);margin-bottom:5px}
.today-name{font-size:22px;font-weight:500;color:var(--text);margin-bottom:2px}
.today-focus{font-size:12px;color:var(--text3);margin-bottom:14px}
.exercise-row{display:flex;align-items:center;gap:10px;padding:9px 0;border-bottom:0.5px solid var(--border)}
.exercise-row:last-child{border-bottom:none}
.ex-num{font-size:10px;color:var(--text3);width:16px}
.ex-name{font-size:13px;color:var(--text);flex:1}
.ex-rx{font-size:11px;color:var(--text3)}
.btn-gold{background:var(--gold);color:#111;border:none;border-radius:8px;font-size:13px;font-weight:700;letter-spacing:.1em;padding:15px;cursor:pointer;width:100%;margin-top:16px;transition:background .15s;-webkit-appearance:none}
.btn-gold:active{background:var(--gold-dim)}
.btn-gold.done{background:transparent;color:var(--green);border:1.5px solid var(--green);font-weight:600}
.btn-outline{background:none;border:0.5px solid var(--border2);border-radius:6px;color:var(--text2);font-size:11px;padding:7px 12px;cursor:pointer}
.btn-back{background:none;border:0.5px solid var(--border);border-radius:6px;color:var(--text3);padding:6px 10px;font-size:11px;cursor:pointer}
.rest-day{text-align:center;padding:28px 16px 16px}
.rest-title{font-size:18px;font-weight:500;color:var(--text);margin-bottom:5px}
.rest-sub{font-size:13px;color:var(--text3);margin-bottom:20px}
.next-card{background:var(--bg2);border:0.5px solid var(--border);border-radius:10px;padding:14px;text-align:left}
.next-label{font-size:9px;letter-spacing:.12em;color:var(--text3);margin-bottom:5px}
.next-name{font-size:15px;font-weight:500;color:var(--text);margin-bottom:2px}
.next-focus{font-size:12px;color:var(--text3);margin-bottom:6px}
.next-when{font-size:12px;color:var(--blue);margin-bottom:10px}
.next-exercises{padding-top:10px;border-top:0.5px solid var(--border)}
.sess-row{display:flex;align-items:center;justify-content:space-between;padding:10px 0;border-bottom:0.5px solid var(--border)}
.sess-row:last-child{border-bottom:none}
.sess-day{font-size:9px;color:var(--text3);width:36px}
.sess-info{flex:1}
.sess-name{font-size:13px;font-weight:500;color:var(--text)}
.sess-focus{font-size:11px;color:var(--text3);margin-top:1px}
.sess-act{font-size:11px;color:var(--gold);cursor:pointer;padding:5px 10px;border:0.5px solid var(--border2);border-radius:5px;background:none}
.sess-act.done{color:var(--green);border-color:var(--green)}

/* SCHEDULE CALENDAR */
.view-toggle{display:flex;border:0.5px solid var(--border2);border-radius:6px;overflow:hidden;width:fit-content;margin-bottom:14px}
.view-toggle button{background:none;border:none;color:var(--text3);font-size:11px;letter-spacing:.06em;padding:6px 14px;cursor:pointer}
.view-toggle button.active{background:var(--gold-bg);color:var(--gold)}
.month-hdr{display:flex;align-items:center;justify-content:space-between;margin-bottom:8px}
.month-title{font-size:13px;font-weight:500;color:var(--text);letter-spacing:.04em}
.month-nav{background:none;border:0.5px solid var(--border2);border-radius:5px;color:var(--text2);padding:4px 12px;cursor:pointer;font-size:16px}
.cal-hdr-row{display:grid;grid-template-columns:repeat(7,1fr);gap:2px;margin-bottom:2px}
.cal-hdr-cell{font-size:9px;color:var(--text3);text-align:center;padding:4px 0;letter-spacing:.06em}
.cal-body{display:grid;grid-template-columns:repeat(7,1fr);gap:2px}
.cal-day{min-height:44px;border-radius:6px;border:0.5px solid transparent;background:var(--bg2);display:flex;flex-direction:column;align-items:center;padding:5px 2px;cursor:default;transition:border-color .15s}
.cal-day.other-month{background:transparent}
.cal-day.other-month .cal-day-num{color:var(--bg3)}
.cal-day.today .cal-day-num{color:var(--gold);font-weight:700}
.cal-day.today{border-color:var(--border2)}
.cal-day.has-sess{border-color:var(--border2);cursor:pointer}
.cal-day.has-sess:active{border-color:var(--gold)}
.cal-day.logged{border-color:var(--green)!important;background:rgba(76,175,125,0.06)}
.cal-day-num{font-size:11px;color:var(--text2);margin-bottom:3px}
.cal-sess-pill{font-size:9px;font-weight:700;border-radius:3px;padding:1px 5px;letter-spacing:.05em;background:var(--gold-bg);color:var(--gold);border:0.5px solid var(--gold)}
.cal-day.logged .cal-sess-pill{background:rgba(76,175,125,0.15);color:var(--green);border-color:var(--green)}

/* LOG */
.lift-block{background:var(--bg2);border:0.5px solid var(--border);border-radius:10px;padding:12px;margin-bottom:10px}
.lift-hdr{display:flex;justify-content:space-between;align-items:center;margin-bottom:5px}
.lift-title{font-size:11px;letter-spacing:.08em;color:var(--text2);font-weight:500}
.lift-rx{font-size:10px;color:var(--text3)}
.lift-calc{font-size:12px;color:var(--gold);margin-bottom:8px}
.set-hdr-row{display:grid;grid-template-columns:22px 1fr 1fr 40px 30px 26px;gap:4px;margin-bottom:4px}
.set-hdr-row span{font-size:9px;letter-spacing:.07em;color:var(--text3);text-align:center}
.set-row-g{display:grid;grid-template-columns:22px 1fr 1fr 40px 30px 26px;gap:4px;margin-bottom:5px;align-items:center}
.set-num{font-size:11px;color:var(--text3);text-align:center}
.set-inp{background:var(--bg3);border:0.5px solid var(--border2);border-radius:5px;color:var(--text);font-size:16px;padding:8px 4px;text-align:center;width:100%;-moz-appearance:textfield;-webkit-appearance:none}
.set-inp:focus{outline:none;border-color:var(--gold)}
.set-inp.target{color:var(--gold)}
.rpe-sel{background:var(--bg3);border:0.5px solid var(--border2);border-radius:5px;color:var(--text2);font-size:11px;padding:8px 2px;width:100%;-webkit-appearance:none}
.rpe-sel:focus{outline:none;border-color:var(--gold)}
.fail-btn{background:none;border:0.5px solid var(--border);border-radius:4px;color:var(--text3);font-size:10px;padding:6px 2px;cursor:pointer;width:100%;text-align:center}
.fail-btn.failed{border-color:var(--red);color:var(--red)}
.rm-set-btn{background:none;border:none;color:var(--text3);font-size:18px;cursor:pointer;padding:0;line-height:1;width:100%;text-align:center}
.set-actions{display:flex;gap:10px;margin-top:6px;flex-wrap:wrap}
.set-action-btn{background:none;border:none;color:var(--text3);font-size:11px;cursor:pointer;padding:4px 0;letter-spacing:.05em}
.set-action-btn.gold{color:var(--gold)}
.vol-bar{background:var(--bg3);border-radius:4px;height:5px;margin-top:6px;overflow:hidden}
.vol-fill{background:var(--gold);height:5px;border-radius:4px;transition:width .3s}
.notes-ta{background:var(--bg3);border:0.5px solid var(--border2);border-radius:6px;color:var(--text2);font-size:14px;padding:8px 10px;width:100%;resize:none;height:60px;font-family:inherit;margin-top:8px;-webkit-appearance:none}
.notes-ta:focus{outline:none;border-color:var(--gold)}
.notes-ta::placeholder{color:var(--text3)}
.media-section{margin-top:12px}
.media-label{font-size:9px;letter-spacing:.12em;color:var(--text3);margin-bottom:8px}
.media-row{display:flex;gap:8px;flex-wrap:wrap}
.media-thumb{width:72px;height:72px;border-radius:6px;object-fit:cover;border:0.5px solid var(--border);cursor:pointer}
.media-add-btns{display:flex;gap:6px;margin-top:8px}
.media-add-btn{flex:1;background:var(--bg3);border:0.5px solid var(--border2);border-radius:6px;color:var(--text2);font-size:11px;padding:10px 6px;cursor:pointer;text-align:center}

/* 1RMs */
.rm-grid{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:8px;margin-bottom:16px}
.rm-card{background:var(--bg2);border:0.5px solid var(--border);border-radius:8px;padding:11px 12px}
.rm-lift{font-size:9px;letter-spacing:.1em;color:var(--text3);margin-bottom:4px}
.rm-val{font-size:20px;font-weight:500;color:var(--gold)}
.rm-val span{font-size:11px;color:var(--text3);font-weight:400}
.rm-input{background:var(--bg3);border:0.5px solid var(--gold);border-radius:5px;color:var(--text);font-size:16px;padding:6px 6px;width:80px;text-align:center;-moz-appearance:textfield;-webkit-appearance:none}
.rm-input:focus{outline:none}
.calc-row{display:flex;gap:8px;align-items:center;margin-bottom:8px}
.calc-inp{background:var(--bg2);border:0.5px solid var(--border2);border-radius:6px;color:var(--text);font-size:14px;padding:9px 10px;flex:1;-moz-appearance:textfield;-webkit-appearance:none}
.calc-inp:focus{outline:none;border-color:var(--gold)}
.calc-result{font-size:13px;color:var(--gold);font-weight:500;min-width:46px}

/* PROGRESS */
.chart-wrap{background:var(--bg2);border:0.5px solid var(--border);border-radius:10px;padding:12px;margin-bottom:14px;height:160px;position:relative}
.pill-row{display:flex;gap:5px;flex-wrap:wrap;margin-bottom:10px}
.pill{background:var(--bg2);border:0.5px solid var(--border);border-radius:20px;color:var(--text3);font-size:10px;padding:5px 11px;cursor:pointer;transition:all .15s}
.pill.active{background:var(--gold-bg);border-color:var(--gold);color:var(--gold)}
.history-row{padding:10px 0;border-bottom:0.5px solid var(--border)}
.history-row:last-child{border-bottom:none}
.hist-media{display:flex;gap:4px;margin-top:6px;flex-wrap:wrap}
.hist-thumb{width:56px;height:56px;border-radius:5px;object-fit:cover;border:0.5px solid var(--border);cursor:pointer}
.weigh-row{display:flex;align-items:center;gap:8px;margin-bottom:8px}
.weigh-lbl{font-size:11px;color:var(--text3);width:50px}
.weigh-inp{background:var(--bg3);border:0.5px solid var(--border2);border-radius:6px;color:var(--text);font-size:14px;padding:9px 8px;flex:1;-moz-appearance:textfield;-webkit-appearance:none}
.weigh-inp:focus{outline:none;border-color:var(--gold)}
.weigh-save{background:none;border:0.5px solid var(--border2);border-radius:5px;color:var(--text2);font-size:11px;padding:8px 12px;cursor:pointer}

/* TIMER */
.timer-wrap{background:var(--bg2);border:0.5px solid var(--border);border-radius:12px;padding:20px 16px;margin-bottom:12px}
.timer-ring-wrap{display:flex;justify-content:center;margin-bottom:16px;position:relative;height:160px}
.timer-ring-wrap svg{transform:rotate(-90deg)}
.timer-ring-track{fill:none;stroke:var(--bg3);stroke-width:6}
.timer-ring-fill{fill:none;stroke:var(--gold);stroke-width:6;stroke-linecap:round;transition:stroke-dashoffset .5s linear}
.timer-ring-fill.done{stroke:var(--green)}
.timer-center{position:absolute;top:50%;left:50%;transform:translate(-50%,-50%);text-align:center}
.timer-display{font-size:36px;font-weight:500;color:var(--gold);letter-spacing:.04em;line-height:1}
.timer-display.done{color:var(--green)}
.timer-sub{font-size:9px;letter-spacing:.12em;color:var(--text3);margin-top:3px}
.timer-presets{display:flex;gap:6px;justify-content:center;flex-wrap:wrap;margin-bottom:12px}
.timer-preset-btn{background:var(--bg3);border:0.5px solid var(--border2);border-radius:6px;color:var(--text2);font-size:11px;padding:8px 12px;cursor:pointer;transition:all .15s}
.timer-preset-btn.active{border-color:var(--gold);color:var(--gold);background:var(--gold-bg)}
.timer-custom-row{display:flex;align-items:center;gap:10px;margin-bottom:16px;justify-content:center}
.timer-custom-lbl{font-size:10px;color:var(--text3);letter-spacing:.08em}
.timer-custom-inp{background:var(--bg3);border:0.5px solid var(--border2);border-radius:6px;color:var(--text);font-size:14px;padding:8px 10px;width:76px;text-align:center;-moz-appearance:textfield;-webkit-appearance:none}
.timer-custom-inp:focus{outline:none;border-color:var(--gold)}
.timer-custom-unit{font-size:10px;color:var(--text3)}
.timer-btns{display:flex;gap:8px;justify-content:center;margin-bottom:14px}
.timer-btn{background:var(--bg3);border:0.5px solid var(--border2);border-radius:10px;color:var(--text2);font-size:22px;padding:12px 20px;cursor:pointer;min-width:60px;line-height:1}
.timer-btn.primary{border-color:var(--gold);color:var(--gold);background:var(--gold-bg)}
.toggle-row{display:flex;align-items:center;gap:8px;justify-content:center;font-size:11px;color:var(--text3)}
.toggle-sw{width:36px;height:20px;background:var(--bg3);border:0.5px solid var(--border2);border-radius:10px;cursor:pointer;position:relative;flex-shrink:0}
.toggle-sw.on{background:var(--gold)}
.toggle-knob{width:14px;height:14px;background:#fff;border-radius:50%;position:absolute;top:2px;left:2px;transition:left .2s}
.toggle-sw.on .toggle-knob{left:18px}

/* LIGHTBOX */
.lightbox{display:none;position:fixed;inset:0;background:rgba(0,0,0,.92);z-index:1000;align-items:center;justify-content:center}
.lightbox.show{display:flex}
.lightbox img{max-width:92vw;max-height:88vh;border-radius:8px;object-fit:contain}
.lightbox-close{position:absolute;top:calc(16px + env(safe-area-inset-top));right:16px;background:none;border:none;color:#fff;font-size:32px;cursor:pointer;padding:8px}

.toast{position:fixed;bottom:calc(24px + env(safe-area-inset-bottom));left:50%;transform:translateX(-50%);background:var(--gold);color:#111;padding:10px 20px;border-radius:20px;font-size:12px;font-weight:600;letter-spacing:.08em;opacity:0;transition:opacity .3s;pointer-events:none;white-space:nowrap;z-index:999}
.toast.show{opacity:1}
.empty{text-align:center;padding:32px 16px;color:var(--text3);font-size:12px;line-height:2}
input::-webkit-outer-spin-button,input::-webkit-inner-spin-button{-webkit-appearance:none}
</style>
</head>
<body>
<div class="app" id="app">
  <div class="hdr">
    <div class="hdr-top">
      <div class="logo-main">JACKED SUMMER 2026</div>
      <button class="mode-btn" onclick="toggleMode()" id="modeBtn">☀</button>
    </div>
    <div class="prog-row">
      <div id="weekChip" class="week-chip">W1</div>
      <div class="sess-dots" id="sessDots"></div>
      <div class="prog-bar-bg"><div class="prog-bar-fill" id="progBarFill" style="width:0%"></div></div>
      <div class="prog-label" id="progBarLabel">0/48</div>
    </div>
  </div>
  <nav class="nav">
    <button class="active" id="navHome" onclick="go('home')">TODAY</button>
    <button id="navCalendar" onclick="go('calendar')">SCHEDULE</button>
    <button id="navLog" onclick="go('log')">LOG</button>
    <button id="navLifts" onclick="go('lifts')">1RMs</button>
    <button id="navProgress" onclick="go('progress')">PROGRESS</button>
    <button id="navTimer" onclick="go('timer')">TIMER</button>
  </nav>
  <div class="content" id="content"></div>
  <div class="toast" id="toast"></div>
  <div class="lightbox" id="lightbox" onclick="closeLightbox()">
    <button class="lightbox-close" onclick="closeLightbox()">×</button>
    <img id="lightboxImg" src="" alt="media" />
  </div>
</div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/4.4.1/chart.umd.min.js"></script>
<script>
const KEY='arc_v7';
const DELOAD_WEEKS=[4,8,12];
const DAY_LABELS=['Mon','Tue','Wed','Thu','Fri','Sat','Sun'];
const DAY_SHORT=['Mo','Tu','We','Th','Fr','Sa','Su'];
const NAV_IDS=['navHome','navCalendar','navLog','navLifts','navProgress','navTimer'];
const MONTHS=['January','February','March','April','May','June','July','August','September','October','November','December'];

const SESSION_TEMPLATES=[
  {letter:'A',focus:'Snatch focus',exercises:[{name:'Snatch',sets:5,reps:3,pct:75},{name:'Snatch pull',sets:4,reps:3,pct:90},{name:'Overhead squat',sets:3,reps:5,pct:70},{name:'Back squat',sets:4,reps:4,pct:80}]},
  {letter:'B',focus:'Clean & Jerk focus',exercises:[{name:'Clean & Jerk',sets:5,reps:2,pct:78},{name:'Clean pull',sets:4,reps:3,pct:90},{name:'Front squat',sets:3,reps:4,pct:80},{name:'Romanian deadlift',sets:3,reps:5,pct:65}]},
  {letter:'C',focus:'Technique & power',exercises:[{name:'Power snatch',sets:5,reps:3,pct:70},{name:'Power clean',sets:4,reps:3,pct:72},{name:'Snatch balance',sets:3,reps:3,pct:65},{name:'Back squat',sets:3,reps:5,pct:75}]},
  {letter:'D',focus:'Strength',exercises:[{name:'Clean & Jerk',sets:4,reps:2,pct:82},{name:'Snatch',sets:4,reps:2,pct:80},{name:'Front squat',sets:4,reps:3,pct:85},{name:'Deadlift',sets:3,reps:4,pct:80}]}
];

function sn(week,letter){return `${week}${letter}`;}

function defaultData(){
  const start=new Date();start.setHours(0,0,0,0);
  const sched=[];
  for(let w=1;w<=12;w++){
    const anchor=new Date(start);anchor.setDate(start.getDate()+(w-1)*7);
    const dow=anchor.getDay();const toMon=dow===0?-6:1-dow;
    const mon=new Date(anchor);mon.setDate(anchor.getDate()+toMon);
    [0,1,3,4].forEach((o,i)=>{
      const d=new Date(mon);d.setDate(mon.getDate()+o);
      sched.push({id:`w${w}s${i}`,week:w,sessionIdx:i,date:d.toISOString().split('T')[0]});
    });
  }
  return{startDate:start.toISOString(),schedule:sched,sessions:{},
    prs:{'Snatch':{kg:45,date:'Test week'},'Clean & Jerk':{kg:60,date:'Test week'},'Back Squat':{kg:95,date:'Test week'},'Front Squat':{kg:null,date:null},'Overhead squat':{kg:null,date:null},'Deadlift':{kg:null,date:null}},
    bodyweight:[],editingRM:null,darkMode:true,schedView:'cal',calViewMonth:null};
}

function load(){try{const r=localStorage.getItem(KEY);return r?JSON.parse(r):null;}catch(e){return null;}}
function save(){try{localStorage.setItem(KEY,JSON.stringify(D));}catch(e){}}

let D=load()||defaultData();
if(!D.schedView)D.schedView='cal';
if(!D.calViewMonth){const n=new Date();D.calViewMonth={y:n.getFullYear(),m:n.getMonth()};}

let tab='home',logState=null;
let timerInterval=null,timerSeconds=120,timerRunning=false,timerAutoStart=true,timerPreset=120,timerTotal=120;
let progressLift='Snatch',progressChart=null,weighChart=null,dragSrcId=null;

function currentWeek(){const s=new Date(D.startDate),n=new Date();return Math.min(Math.max(Math.floor((n-s)/(1000*60*60*24*7))+1,1),12);}
function isDeload(w){return DELOAD_WEEKS.includes(w);}
function todayStr(){return new Date().toISOString().split('T')[0];}
function fmt(n){return n!==null&&n!==undefined&&n!==''?parseFloat(n).toFixed(1).replace(/\.0$/,''):'—';}
function round5(n){return Math.round(n/2.5)*2.5;}
function pctCalc(liftName,pct){
  const k=Object.keys(D.prs).find(k=>k.toLowerCase()===liftName.toLowerCase());
  const pr=k?D.prs[k]:null;
  if(!pr||!pr.kg)return null;
  return round5(pr.kg*(pct/100));
}

function toggleMode(){
  D.darkMode=!D.darkMode;save();
  document.getElementById('app').className=D.darkMode?'app':'app lm';
  document.getElementById('modeBtn').textContent=D.darkMode?'☀':'🌙';
}

function go(t){
  tab=t;logState=null;
  NAV_IDS.forEach(id=>document.getElementById(id).classList.remove('active'));
  const map={home:'navHome',calendar:'navCalendar',log:'navLog',lifts:'navLifts',progress:'navProgress',timer:'navTimer'};
  document.getElementById(map[t]).classList.add('active');
  if(progressChart){progressChart.destroy();progressChart=null;}
  if(weighChart){weighChart.destroy();weighChart=null;}
  render();
}

function showToast(msg){const el=document.getElementById('toast');el.textContent=msg;el.classList.add('show');setTimeout(()=>el.classList.remove('show'),2200);}

function updateHeader(){
  const w=currentWeek();
  const chip=document.getElementById('weekChip');
  chip.textContent=isDeload(w)?`W${w}✦`:`W${w}`;
  chip.className=isDeload(w)?'deload-chip':'week-chip';
  document.getElementById('app').className=D.darkMode?'app':'app lm';
  document.getElementById('modeBtn').textContent=D.darkMode?'☀':'🌙';
  const done=Object.keys(D.sessions).length;
  document.getElementById('progBarFill').style.width=Math.round(done/48*100)+'%';
  document.getElementById('progBarLabel').textContent=`${done}/48`;
  const today=todayStr();
  const wSessions=D.schedule.filter(s=>s.week===w).sort((a,b)=>a.date.localeCompare(b.date));
  const nextUndoneId=wSessions.find(s=>!D.sessions[s.id]&&s.date>=today)?.id||wSessions.find(s=>!D.sessions[s.id])?.id;
  const dotsHtml=wSessions.map(s=>{
    const t=SESSION_TEMPLATES[s.sessionIdx];
    const logged=!!D.sessions[s.id];
    const isNext=s.id===nextUndoneId;
    let cls='sdot';
    if(logged)cls+=' done';
    else if(isNext)cls+=' next';
    return `<div class="${cls}">${t.letter}</div>`;
  }).join('');
  document.getElementById('sessDots').innerHTML=dotsHtml;
}

function render(){
  updateHeader();
  const c=document.getElementById('content');
  if(tab==='home')renderHome(c);
  else if(tab==='calendar')renderCalendar(c);
  else if(tab==='log'){if(logState)renderLogForm(c);else renderLogPicker(c);}
  else if(tab==='lifts')renderLifts(c);
  else if(tab==='progress')renderProgress(c);
  else if(tab==='timer')renderTimer(c);
}

function getTodaySession(){return D.schedule.find(s=>s.date===todayStr());}
function getNextSession(){return D.schedule.filter(s=>s.date>todayStr()).sort((a,b)=>a.date.localeCompare(b.date))[0]||null;}
function daysUntil(ds){const n=new Date();n.setHours(0,0,0,0);return Math.round((new Date(ds)-n)/(1000*60*60*24));}

function renderHome(c){
  const w=currentWeek();const todaySess=getTodaySession();
  if(todaySess){
    const t=SESSION_TEMPLATES[todaySess.sessionIdx];const logged=D.sessions[todaySess.id];const deload=isDeload(todaySess.week);
    const exRows=t.exercises.map((ex,i)=>{
      const target=pctCalc(ex.name,ex.pct);
      return `<div class="exercise-row"><div class="ex-num">${i+1}</div><div class="ex-name">${ex.name}</div><div class="ex-rx">${ex.sets}×${ex.reps}${target?` · <span style="color:var(--gold)">${fmt(target)}kg</span>`:`· ${ex.pct}%`}</div></div>`;
    }).join('');
    c.innerHTML=`<div class="today-session"><div class="today-label">TODAY${deload?' · DELOAD':''}</div><div class="today-name">${sn(todaySess.week,t.letter)}</div><div class="today-focus">${t.focus}</div><div>${exRows}</div><button class="btn-gold ${logged?'done':''}" onclick="openLog('${todaySess.id}')">${logged?'✓ LOGGED — EDIT SESSION':'START SESSION'}</button></div><p class="sec-label">THIS WEEK</p><div class="card">${weekMiniList(w)}</div>`;
  } else {
    const next=getNextSession();
    let nextHtml='';
    if(next){
      const t=SESSION_TEMPLATES[next.sessionIdx];const days=daysUntil(next.date);
      const d=new Date(next.date);const dayName=DAY_LABELS[d.getDay()===0?6:d.getDay()-1];
      const dateLabel=d.toLocaleDateString('en-GB',{day:'numeric',month:'short'});
      const exPrev=t.exercises.map(ex=>`<div style="font-size:12px;color:var(--text3);padding:5px 0;border-bottom:0.5px solid var(--border)">${ex.name}<span style="float:right">${ex.sets}×${ex.reps}</span></div>`).join('');
      nextHtml=`<div class="next-card"><div class="next-label">NEXT SESSION</div><div class="next-name">${sn(next.week,t.letter)}</div><div class="next-focus">${t.focus}</div><div class="next-when">${days===0?'Today':days===1?'Tomorrow':`In ${days} days`} · ${dayName} ${dateLabel}</div><div class="next-exercises">${exPrev}</div></div>`;
    }
    c.innerHTML=`<div class="rest-day"><div class="rest-title">Rest day</div><div class="rest-sub">Recovery is part of the program.</div>${nextHtml}</div><p class="sec-label" style="margin-top:8px">THIS WEEK</p><div class="card">${weekMiniList(w)}</div>`;
  }
}

function weekMiniList(w){
  return D.schedule.filter(s=>s.week===w).sort((a,b)=>a.date.localeCompare(b.date)).map(s=>{
    const t=SESSION_TEMPLATES[s.sessionIdx];const logged=D.sessions[s.id];
    const d=new Date(s.date);const dayName=DAY_LABELS[d.getDay()===0?6:d.getDay()-1];
    const isToday=s.date===todayStr();
    return `<div class="sess-row"><div class="sess-day" style="${isToday?'color:var(--gold)':''}">${dayName}</div><div class="sess-info"><div class="sess-name" style="font-size:13px">${sn(w,t.letter)}</div><div class="sess-focus">${t.focus}</div></div><button class="sess-act ${logged?'done':''}" onclick="openLog('${s.id}')">${logged?'✓':'Log'}</button></div>`;
  }).join('');
}

function renderCalendar(c){
  const isCalView=D.schedView==='cal';
  const toggle=`<div class="view-toggle"><button class="${isCalView?'active':''}" onclick="D.schedView='cal';save();renderCalendar(document.getElementById('content'))">CAL</button><button class="${!isCalView?'active':''}" onclick="D.schedView='list';save();renderCalendar(document.getElementById('content'))">LIST</button></div>`;
  if(isCalView){
    const {y,m}=D.calViewMonth;
    const firstDay=new Date(y,m,1);
    const startDow=firstDay.getDay()===0?6:firstDay.getDay()-1;
    const gridStart=new Date(firstDay);gridStart.setDate(gridStart.getDate()-startDow);
    const cells=[];for(let i=0;i<42;i++){const d=new Date(gridStart);d.setDate(gridStart.getDate()+i);cells.push(d);}
    const today=todayStr();
    const hdrCells=DAY_SHORT.map(d=>`<div class="cal-hdr-cell">${d}</div>`).join('');
    const bodyCells=cells.map(d=>{
      const ds=d.toISOString().split('T')[0];const inMonth=d.getMonth()===m;
      const sched=D.schedule.find(s=>s.date===ds);const logged=sched?!!D.sessions[sched.id]:false;
      const t=sched?SESSION_TEMPLATES[sched.sessionIdx]:null;
      let cls='cal-day';if(!inMonth)cls+=' other-month';if(ds===today)cls+=' today';
      if(sched&&logged)cls+=' logged';else if(sched)cls+=' has-sess';
      const pill=sched?`<div class="cal-sess-pill">${sn(sched.week,t.letter)}</div>`:'';
      return `<div class="${cls}" onclick="${sched?`openLog('${sched.id}')`:''}" title="${sched?sn(sched.week,t.letter):''}"><div class="cal-day-num">${d.getDate()}</div>${pill}</div>`;
    }).join('');
    c.innerHTML=`${toggle}<div class="month-hdr"><button class="month-nav" onclick="changeMonth(-1)">‹</button><div class="month-title">${MONTHS[m]} ${y}</div><button class="month-nav" onclick="changeMonth(1)">›</button></div><div class="cal-hdr-row">${hdrCells}</div><div class="cal-body">${bodyCells}</div><div style="margin-top:12px;display:flex;gap:12px;font-size:10px;color:var(--text3)"><span><span style="color:var(--gold)">■</span> Scheduled</span><span><span style="color:var(--green)">■</span> Logged</span></div>`;
  } else {
    const today=todayStr();let html='';
    for(let wk=1;wk<=12;wk++){
      const sessions=D.schedule.filter(s=>s.week===wk).sort((a,b)=>a.date.localeCompare(b.date));
      const dlabel=isDeload(wk)?` <span style="font-size:9px;color:var(--gold)">DELOAD</span>`:'';
      const rows=sessions.map(s=>{
        const t=SESSION_TEMPLATES[s.sessionIdx];const logged=D.sessions[s.id];
        const d=new Date(s.date);const dayName=DAY_LABELS[d.getDay()===0?6:d.getDay()-1];
        const dateLabel=d.toLocaleDateString('en-GB',{day:'numeric',month:'short'});
        const isPast=s.date<today;
        return `<div class="sess-row"><div class="sess-day" style="width:40px;line-height:1.4;${s.date===today?'color:var(--gold)':''}">${dayName}<br><span style="font-size:9px;color:var(--text3)">${dateLabel}</span></div><div class="sess-info"><div class="sess-name" style="font-size:12px">${sn(wk,t.letter)}</div><div class="sess-focus">${t.focus}</div></div><button class="sess-act ${logged?'done':''}" onclick="openLog('${s.id}')">${logged?'✓':isPast?'Late':'Log'}</button></div>`;
      }).join('');
      html+=`<div style="margin-bottom:10px"><p class="sec-label">WEEK ${wk}${dlabel}</p><div class="card" style="padding:4px 14px">${rows}</div></div>`;
    }
    c.innerHTML=`${toggle}${html}`;
  }
}

function changeMonth(dir){
  let {y,m}=D.calViewMonth;m+=dir;if(m>11){m=0;y++;}if(m<0){m=11;y--;}
  D.calViewMonth={y,m};save();renderCalendar(document.getElementById('content'));
}

function dragStart(e,id){if(!id)return;dragSrcId=id;}
function dragOver(e){e.preventDefault();e.currentTarget.classList.add('drag-over');}
function dragLeave(e){e.currentTarget.classList.remove('drag-over');}
function dragDrop(e,ds){
  e.preventDefault();e.currentTarget.classList.remove('drag-over');
  if(!dragSrcId)return;
  const existing=D.schedule.find(s=>s.date===ds&&s.id!==dragSrcId);
  const src=D.schedule.find(s=>s.id===dragSrcId);if(!src)return;
  if(existing){const tmp=existing.date;existing.date=src.date;src.date=tmp;}else src.date=ds;
  dragSrcId=null;save();render();showToast('Schedule updated');
}

function openLog(id){
  const sched=D.schedule.find(s=>s.id===id);if(!sched)return;
  const t=SESSION_TEMPLATES[sched.sessionIdx];const existing=D.sessions[id];
  logState={id,sched,template:t,sets:t.exercises.map((ex,ei)=>({exercise:ex,rows:existing?JSON.parse(JSON.stringify(existing.sets[ei]?.rows||[]))||buildRows(ex):buildRows(ex)})),notes:existing?.notes||'',media:existing?.media||[]};
  tab='log';NAV_IDS.forEach(id=>document.getElementById(id).classList.remove('active'));document.getElementById('navLog').classList.add('active');render();
}
function buildRows(ex){return Array.from({length:ex.sets},()=>({reps:'',kg:'',rpe:'',failed:false}));}

function renderLogPicker(c){
  const w=currentWeek();
  const html=D.schedule.filter(s=>s.week===w).sort((a,b)=>a.date.localeCompare(b.date)).map(s=>{
    const t=SESSION_TEMPLATES[s.sessionIdx];const logged=D.sessions[s.id];
    const d=new Date(s.date);const dayName=DAY_LABELS[d.getDay()===0?6:d.getDay()-1];
    return `<div class="sess-row"><div class="sess-day">${dayName}</div><div class="sess-info"><div class="sess-name">${sn(w,t.letter)}</div><div class="sess-focus">${t.focus}${isDeload(w)?' · deload':''}</div></div><button class="sess-act ${logged?'done':''}" onclick="openLog('${s.id}')">${logged?'✓ Redo':'Log'}</button></div>`;
  }).join('');
  c.innerHTML=`<p class="sec-label">WEEK ${w} SESSIONS</p><div class="card">${html}</div>`;
}

function renderLogForm(c){
  const t=logState.template;const d=new Date(logState.sched.date);
  const dayName=DAY_LABELS[d.getDay()===0?6:d.getDay()-1];const dateLabel=d.toLocaleDateString('en-GB',{day:'numeric',month:'short'});
  const deload=isDeload(logState.sched.week);
  let totalVol=0;logState.sets.forEach(s=>s.rows.forEach(r=>{totalVol+=(parseFloat(r.kg)||0)*(parseFloat(r.reps)||0);}));
  const liftsHtml=logState.sets.map((s,si)=>{
    const ex=s.exercise;const target=pctCalc(ex.name,ex.pct);
    const targetStr=target?`Target: ${fmt(target)}kg (${ex.pct}% 1RM)`:`${ex.pct}% of 1RM`;
    const hasPrev=!!Object.values(D.sessions).find(sess=>sess.templateIdx===logState.sched.sessionIdx);
    const rowsHtml=s.rows.map((r,ri)=>`<div class="set-row-g"><div class="set-num">${ri+1}</div><input class="set-inp target" type="number" inputmode="decimal" step="0.5" placeholder="${target?fmt(target):'kg'}" value="${r.kg}" oninput="setVal(${si},${ri},'kg',this.value)" /><input class="set-inp" type="number" inputmode="numeric" step="1" placeholder="${ex.reps}" value="${r.reps}" oninput="setVal(${si},${ri},'reps',this.value)" /><select class="rpe-sel" onchange="setVal(${si},${ri},'rpe',this.value)"><option value="">—</option>${[6,6.5,7,7.5,8,8.5,9,9.5,10].map(v=>`<option value="${v}" ${r.rpe==v?'selected':''}>${v}</option>`).join('')}</select><button class="fail-btn ${r.failed?'failed':''}" onclick="toggleFail(${si},${ri})">${r.failed?'MISS':'—'}</button><button class="rm-set-btn" onclick="removeSet(${si},${ri})">×</button></div>`).join('');
    return `<div class="lift-block"><div class="lift-hdr"><div class="lift-title">${ex.name.toUpperCase()}</div><div class="lift-rx">${ex.sets}×${ex.reps}${deload?' · deload':''}</div></div><div class="lift-calc">${targetStr}</div><div class="set-hdr-row"><span></span><span>KG</span><span>REPS</span><span>RPE</span><span>MISS</span><span></span></div>${rowsHtml}<div class="set-actions"><button class="set-action-btn" onclick="addSet(${si})">+ add set</button><button class="set-action-btn gold" onclick="duplicateLastSet(${si})">⊕ duplicate last</button>${hasPrev?`<button class="set-action-btn gold" onclick="quickFill(${si})">↑ last session</button>`:''}</div></div>`;
  }).join('');
  const mediaThumbs=logState.media.map(m=>`<img class="media-thumb" src="${m.data}" onclick="openLightbox('${m.data}')" alt="media" />`).join('');
  c.innerHTML=`<div style="display:flex;align-items:center;gap:8px;margin-bottom:12px"><button class="btn-back" onclick="logState=null;render()">← back</button><div><div style="font-size:15px;font-weight:500;color:var(--text)">${sn(logState.sched.week,t.letter)}</div><div style="font-size:10px;color:var(--text3)">${dayName} ${dateLabel}${deload?' · DELOAD':''}</div></div></div><div style="margin-bottom:14px"><div style="display:flex;justify-content:space-between;align-items:baseline;margin-bottom:4px"><span style="font-size:9px;letter-spacing:.12em;color:var(--text3)">SESSION VOLUME</span><span style="font-size:16px;font-weight:500;color:var(--gold)" id="volDisplay">${Math.round(totalVol).toLocaleString()}kg</span></div><div class="vol-bar"><div class="vol-fill" id="volFill" style="width:${Math.min(totalVol/2000*100,100).toFixed(0)}%"></div></div></div>${liftsHtml}<textarea class="notes-ta" placeholder="Session notes, technique cues…" oninput="logState.notes=this.value">${logState.notes}</textarea><div class="media-section"><div class="media-label">SESSION MEDIA</div><div class="media-row">${mediaThumbs}</div><div class="media-add-btns" style="margin-top:8px"><button class="media-add-btn" onclick="triggerMedia('camera')">📷 Camera</button><button class="media-add-btn" onclick="triggerMedia('library')">🖼 Library</button></div><input type="file" id="mediaInput" accept="image/*,video/*" style="display:none" onchange="handleMediaUpload(event)" /></div><button class="btn-gold" style="margin-top:12px" onclick="saveSession()">SAVE SESSION</button>`;
}

function setVal(si,ri,field,val){
  logState.sets[si].rows[ri][field]=val;
  let v=0;logState.sets.forEach(s=>s.rows.forEach(r=>{v+=(parseFloat(r.kg)||0)*(parseFloat(r.reps)||0);}));
  const el=document.getElementById('volDisplay');const fill=document.getElementById('volFill');
  if(el)el.textContent=Math.round(v).toLocaleString()+'kg';if(fill)fill.style.width=Math.min(v/2000*100,100).toFixed(0)+'%';
}
function toggleFail(si,ri){logState.sets[si].rows[ri].failed=!logState.sets[si].rows[ri].failed;render();}
function addSet(si){logState.sets[si].rows.push({reps:'',kg:'',rpe:'',failed:false});render();}
function removeSet(si,ri){if(logState.sets[si].rows.length<=1){showToast('Need at least 1 set');return;}logState.sets[si].rows.splice(ri,1);render();}
function duplicateLastSet(si){const rows=logState.sets[si].rows;if(!rows.length)return;rows.push({...rows[rows.length-1]});render();showToast('Set duplicated');}
function quickFill(si){
  const prev=Object.values(D.sessions).filter(s=>s.templateIdx===logState.sched.sessionIdx);if(!prev.length)return;
  const last=prev[prev.length-1];const prevRows=last?.sets?.[si]?.rows;if(!prevRows)return;
  prevRows.forEach((pr,ri)=>{if(logState.sets[si].rows[ri])logState.sets[si].rows[ri].kg=pr.kg;});
  render();showToast('Last weights loaded');
}
function triggerMedia(mode){const inp=document.getElementById('mediaInput');if(mode==='camera')inp.setAttribute('capture','environment');else inp.removeAttribute('capture');inp.click();}
function handleMediaUpload(e){
  const file=e.target.files[0];if(!file)return;
  const reader=new FileReader();
  reader.onload=ev=>{logState.media.push({type:file.type.startsWith('video')?'video':'image',data:ev.target.result,name:file.name});render();showToast('Media added');};
  reader.readAsDataURL(file);e.target.value='';
}
function openLightbox(src){document.getElementById('lightboxImg').src=src;document.getElementById('lightbox').classList.add('show');}
function closeLightbox(){document.getElementById('lightbox').classList.remove('show');}
function saveSession(){
  let vol=0;logState.sets.forEach(s=>s.rows.forEach(r=>{vol+=(parseFloat(r.kg)||0)*(parseFloat(r.reps)||0);}));
  const t=SESSION_TEMPLATES[logState.sched.sessionIdx];
  const sess={id:logState.id,templateIdx:logState.sched.sessionIdx,week:logState.sched.week,name:sn(logState.sched.week,t.letter),date:new Date().toLocaleDateString('en-GB',{day:'numeric',month:'short'}),sets:logState.sets.map(s=>({exercise:s.exercise.name,rows:s.rows})),notes:logState.notes,volume:Math.round(vol),media:logState.media};
  D.sessions[logState.id]=sess;
  logState.sets.forEach(s=>{
    const maxKg=Math.max(...s.rows.map(r=>parseFloat(r.kg)||0));
    if(maxKg>0){
      const k=Object.keys(D.prs).find(k=>k.toLowerCase()===s.exercise.name.toLowerCase())||s.exercise.name;
      if(!D.prs[k])D.prs[k]={};if(!D.prs[k].kg||maxKg>D.prs[k].kg){D.prs[k]={kg:maxKg,date:sess.date};setTimeout(()=>showToast(`New PR — ${k}: ${fmt(maxKg)}kg`),300);}
    }
  });
  save();logState=null;
  if(timerAutoStart){timerSeconds=timerPreset;timerTotal=timerPreset;if(timerInterval)clearInterval(timerInterval);timerRunning=true;timerInterval=setInterval(()=>{if(timerSeconds>0){timerSeconds--;updateTimerRing();}else{clearInterval(timerInterval);timerRunning=false;updateTimerRing();}},1000);}
  go('home');showToast('Session saved');
}

function renderLifts(c){
  const LIFTS=Object.keys(D.prs);
  const rmCards=LIFTS.map(k=>{
    const pr=D.prs[k];const editing=D.editingRM===k;
    return `<div class="rm-card"><div class="rm-lift">${k.toUpperCase()}</div>${editing?`<div style="display:flex;align-items:center;gap:6px;margin-top:4px"><input class="rm-input" type="number" inputmode="decimal" step="0.5" value="${pr?.kg||''}" id="rmi_${k.replace(/[\s&]/g,'_')}" /><button class="btn-outline" style="padding:6px 10px;font-size:11px" onclick="saveRM('${k}')">Save</button></div>`:`<div style="display:flex;align-items:center;justify-content:space-between"><div class="rm-val">${pr?.kg?fmt(pr.kg):'—'}<span>kg</span></div><button style="background:none;border:none;color:var(--text3);cursor:pointer;font-size:16px;padding:4px" onclick="editRM('${k}')">✎</button></div><div style="font-size:10px;color:var(--text3);margin-top:2px">${pr?.date||'not set'}</div>`}</div>`;
  }).join('');
  const pcts=[60,65,70,75,78,80,82,85,88,90,95,100];
  const calcLift=LIFTS.find(k=>D.prs[k]?.kg)||'Snatch';const calcPR=D.prs[calcLift]?.kg;
  const tableRows=calcPR?pcts.map(p=>`<div style="display:flex;justify-content:space-between;padding:8px 0;border-bottom:0.5px solid var(--border);font-size:13px"><span style="color:var(--text3)">${p}%</span><span style="color:var(--gold)">${fmt(round5(calcPR*(p/100)))}kg</span></div>`).join(''):'';
  c.innerHTML=`<p class="sec-label">1 REP MAXES</p><div class="rm-grid">${rmCards}</div><p class="sec-label">% REVERSE CALCULATOR</p><div class="card" style="margin-bottom:12px"><div class="calc-row"><input class="calc-inp" type="number" inputmode="decimal" step="0.5" placeholder="Weight (kg)" id="revKg" oninput="updateRevCalc()" /><input class="calc-inp" type="number" inputmode="decimal" step="0.5" placeholder="1RM (kg)" id="rev1rm" oninput="updateRevCalc()" /><div class="calc-result" id="revResult">—%</div></div><div style="font-size:10px;color:var(--text3)">Leave 1RM blank to use ${calcLift} (${calcPR?fmt(calcPR)+'kg':'not set'})</div></div>${calcPR?`<p class="sec-label">${calcLift.toUpperCase()} TABLE (${fmt(calcPR)}kg)</p><div class="card">${tableRows}</div>`:''}`;
}
function editRM(k){D.editingRM=k;render();}
function saveRM(k){
  const el=document.getElementById('rmi_'+k.replace(/[\s&]/g,'_'));if(!el)return;
  const v=parseFloat(el.value);if(!isNaN(v)&&v>0){D.prs[k]={kg:v,date:new Date().toLocaleDateString('en-GB',{day:'numeric',month:'short'})};save();}
  D.editingRM=null;render();showToast('1RM updated');
}
function updateRevCalc(){
  const kg=parseFloat(document.getElementById('revKg')?.value)||0;
  const calcLift=Object.keys(D.prs).find(k=>D.prs[k]?.kg)||'Snatch';
  const rm=parseFloat(document.getElementById('rev1rm')?.value)||D.prs[calcLift]?.kg||0;
  const el=document.getElementById('revResult');if(el)el.textContent=(kg>0&&rm>0)?Math.round(kg/rm*100)+'%':'—%';
}

function renderProgress(c){
  if(progressChart){progressChart.destroy();progressChart=null;}if(weighChart){weighChart.destroy();weighChart=null;}
  const allLifts=['Snatch','Clean & Jerk','Back Squat','Front Squat','Power Snatch','Power Clean'];
  const pills=allLifts.map(l=>`<button class="pill ${l===progressLift?'active':''}" onclick="progressLift='${l}';renderProgress(document.getElementById('content'))">${l}</button>`).join('');
  const points=[];
  if(progressLift==='Snatch')points.push({label:'Start',kg:45});
  if(progressLift==='Clean & Jerk')points.push({label:'Start',kg:60});
  if(progressLift==='Back Squat')points.push({label:'Start',kg:95});
  Object.values(D.sessions).forEach(s=>{s.sets.forEach(sg=>{if(sg.exercise?.toLowerCase()===progressLift.toLowerCase()){const max=Math.max(...sg.rows.map(r=>parseFloat(r.kg)||0));if(max>0)points.push({label:s.name,kg:max});}});});
  const bwPts=D.bodyweight.map(b=>({label:`W${b.week}`,kg:b.kg}));
  const w=currentWeek();const bwLast=D.bodyweight.length?D.bodyweight[D.bodyweight.length-1]:null;
  const histRows=Object.values(D.sessions).reverse().map(s=>{
    const mediaThumbs=s.media&&s.media.length?`<div class="hist-media">${s.media.map(m=>`<img class="hist-thumb" src="${m.data}" onclick="openLightbox('${m.data}')" alt="media" />`).join('')}</div>`:'';
    return `<div class="history-row"><div style="display:flex;justify-content:space-between;width:100%;align-items:center"><div><div style="font-size:10px;color:var(--text3)">${s.date} · ${s.name}</div><div style="font-size:10px;color:var(--text3);margin-top:2px">${s.volume?s.volume.toLocaleString()+'kg volume':''}</div></div><div style="font-size:11px;color:var(--green)">${s.volume?'✓':''}</div></div>${mediaThumbs}</div>`;
  }).join('');
  c.innerHTML=`<p class="sec-label">LIFT PROGRESSION</p><div class="pill-row">${pills}</div><div class="chart-wrap"><canvas id="progChart"></canvas></div><p class="sec-label">WEEKLY WEIGH-IN</p><div class="card" style="margin-bottom:14px"><div class="weigh-row"><div class="weigh-lbl">Week ${w}</div><input class="weigh-inp" type="number" inputmode="decimal" step="0.1" placeholder="kg" id="bwInput" value="${bwLast&&bwLast.week===w?bwLast.kg:''}" /><button class="weigh-save" onclick="saveWeight()">Save</button></div></div>${bwPts.length?`<div class="chart-wrap"><canvas id="bwChart"></canvas></div>`:''}<p class="sec-label">SESSION HISTORY</p><div class="card">${histRows||'<div class="empty">No sessions logged yet</div>'}</div>`;
  const co={responsive:true,maintainAspectRatio:false,plugins:{legend:{display:false}},scales:{x:{ticks:{color:'#666',font:{size:10}},grid:{color:D.darkMode?'#222':'#ddd'}},y:{ticks:{color:'#666',font:{size:10},callback:v=>v+'kg'},grid:{color:D.darkMode?'#222':'#ddd'}}}};
  if(points.length>0)progressChart=new Chart(document.getElementById('progChart'),{type:'line',data:{labels:points.map(p=>p.label),datasets:[{data:points.map(p=>p.kg),borderColor:'#c8a96e',backgroundColor:'rgba(200,169,110,0.08)',borderWidth:2,pointBackgroundColor:'#c8a96e',pointRadius:4,tension:.3,fill:true}]},options:co});
  if(bwPts.length>0)weighChart=new Chart(document.getElementById('bwChart'),{type:'line',data:{labels:bwPts.map(p=>p.label),datasets:[{data:bwPts.map(p=>p.kg),borderColor:'#4caf7d',backgroundColor:'rgba(76,175,125,0.08)',borderWidth:2,pointBackgroundColor:'#4caf7d',pointRadius:4,tension:.3,fill:true}]},options:co});
}
function saveWeight(){
  const v=parseFloat(document.getElementById('bwInput')?.value);if(!v||isNaN(v))return;
  const w=currentWeek();const date=new Date().toLocaleDateString('en-GB',{day:'numeric',month:'short'});
  const idx=D.bodyweight.findIndex(b=>b.week===w);
  if(idx>=0)D.bodyweight[idx]={week:w,kg:v,date};else D.bodyweight.push({week:w,kg:v,date});
  save();showToast('Weight saved');render();
}

const RING_R=62;const RING_CIRC=2*Math.PI*RING_R;
function ringOffset(){return RING_CIRC*(1-(timerTotal>0?timerSeconds/timerTotal:0));}
function renderTimer(c){
  const m=Math.floor(timerSeconds/60),s=timerSeconds%60;
  const disp=`${String(m).padStart(2,'0')}:${String(s).padStart(2,'0')}`;
  const isDone=timerSeconds===0&&!timerRunning;
  c.innerHTML=`<p class="sec-label">REST TIMER</p><div class="timer-wrap"><div class="timer-ring-wrap"><svg width="144" height="144" viewBox="0 0 144 144"><circle class="timer-ring-track" cx="72" cy="72" r="${RING_R}"/><circle class="timer-ring-fill ${isDone?'done':''}" id="timerRing" cx="72" cy="72" r="${RING_R}" stroke-dasharray="${RING_CIRC.toFixed(2)}" stroke-dashoffset="${ringOffset().toFixed(2)}"/></svg><div class="timer-center"><div class="timer-display ${isDone?'done':''}" id="timerDisp">${disp}</div><div class="timer-sub">${timerRunning?'RESTING':'READY'}</div></div></div><div class="timer-presets">${[60,90,120,180,240,300].map(p=>`<button class="timer-preset-btn ${p===timerPreset?'active':''}" onclick="setPreset(${p})">${p>=60?p/60+'m':p+'s'}</button>`).join('')}</div><div class="timer-custom-row"><span class="timer-custom-lbl">CUSTOM</span><input class="timer-custom-inp" type="number" inputmode="numeric" min="5" max="600" value="${timerPreset}" id="customInp" onchange="setPreset(Math.max(5,Math.min(600,parseInt(this.value)||60)))" /><span class="timer-custom-unit">sec</span></div><div class="timer-btns"><button class="timer-btn" onclick="resetTimer()">↺</button><button class="timer-btn primary" onclick="toggleTimer()" id="timerPlayBtn">${timerRunning?'⏸':'▶'}</button><button class="timer-btn" onclick="addTime(30)">+30</button></div><div class="toggle-row"><span>Auto-start on set save</span><div class="toggle-sw ${timerAutoStart?'on':''}" onclick="timerAutoStart=!timerAutoStart;renderTimer(document.getElementById('content'))"><div class="toggle-knob"></div></div></div></div><div class="card"><div style="font-size:9px;letter-spacing:.12em;color:var(--text3);margin-bottom:8px">OLYMPIC LIFTING REST GUIDE</div><div style="font-size:12px;color:var(--text2);line-height:2.4"><div>Snatch / Clean & Jerk<span style="float:right;color:var(--text3)">3–5 min</span></div><div>Pulls / squats<span style="float:right;color:var(--text3)">2–3 min</span></div><div>Accessory work<span style="float:right;color:var(--text3)">1–2 min</span></div></div></div>`;
}
function setPreset(s){timerPreset=s;timerTotal=s;if(!timerRunning)timerSeconds=s;renderTimer(document.getElementById('content'));}
function toggleTimer(){
  if(timerRunning){clearInterval(timerInterval);timerRunning=false;renderTimer(document.getElementById('content'));return;}
  if(timerSeconds<=0){timerSeconds=timerPreset;timerTotal=timerPreset;}
  timerRunning=true;
  timerInterval=setInterval(()=>{if(timerSeconds>0){timerSeconds--;updateTimerRing();}else{clearInterval(timerInterval);timerRunning=false;updateTimerRing();}},1000);
  renderTimer(document.getElementById('content'));
}
function resetTimer(){clearInterval(timerInterval);timerRunning=false;timerSeconds=timerPreset;timerTotal=timerPreset;renderTimer(document.getElementById('content'));}
function addTime(s){timerSeconds+=s;if(timerTotal<timerSeconds)timerTotal=timerSeconds;updateTimerRing();}
function updateTimerRing(){
  const m=Math.floor(timerSeconds/60),s=timerSeconds%60;const isDone=timerSeconds===0&&!timerRunning;
  const dispEl=document.getElementById('timerDisp');const ringEl=document.getElementById('timerRing');const playEl=document.getElementById('timerPlayBtn');
  if(dispEl){dispEl.textContent=`${String(m).padStart(2,'0')}:${String(s).padStart(2,'0')}`;dispEl.className='timer-display'+(isDone?' done':'');}
  if(ringEl){ringEl.style.strokeDashoffset=ringOffset().toFixed(2);ringEl.className='timer-ring-fill'+(isDone?' done':'');}
  if(playEl)playEl.textContent=timerRunning?'⏸':'▶';
}

document.getElementById('app').className=D.darkMode?'app':'app lm';
render();
</script>
</body>
</html>
