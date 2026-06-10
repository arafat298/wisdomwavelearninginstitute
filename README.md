<!DOCTYPE html>
<html lang="en" data-theme="dark">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>WisdomWave Learning Institute</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;500;600;700&family=Outfit:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<style>
:root{
  --blue:#3b82f6;--blue2:#60a5fa;--blue-glow:rgba(59,130,246,0.18);
  --gold:#c9a84c;--gold2:#e8c96d;--gold-glow:rgba(201,168,76,0.13);
  --green:#22c55e;--red:#ef4444;--purple:#a855f7;
}
[data-theme="dark"]{
  --bg:#050810;--bg2:#080d1a;--bg3:#0d1424;--bg4:#111c30;
  --border:rgba(59,130,246,0.08);--border2:rgba(59,130,246,0.25);--border3:rgba(201,168,76,0.2);
  --text:#e8f0ff;--text2:#6b7fa0;--text3:#2d3f5c;
}
[data-theme="light"]{
  --bg:#f0f4ff;--bg2:#f8fbff;--bg3:#e8effe;--bg4:#dde8fd;
  --border:rgba(59,130,246,0.1);--border2:rgba(59,130,246,0.3);--border3:rgba(201,168,76,0.3);
  --text:#0f1928;--text2:#3d5070;--text3:#8898b8;
}
*{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth}
body{font-family:'Outfit',sans-serif;background:var(--bg);color:var(--text);line-height:1.6;overflow-x:hidden;transition:background .3s,color .3s}

/* ── GLOW EFFECTS ── */
.glow-blue{box-shadow:0 0 30px rgba(59,130,246,.15),0 0 60px rgba(59,130,246,.08)}
.glow-gold{box-shadow:0 0 24px rgba(201,168,76,.2)}

/* ── NAV ── */
nav{position:sticky;top:0;z-index:300;background:rgba(5,8,16,.96);backdrop-filter:blur(24px);border-bottom:1px solid var(--border2);padding:0 5%}
[data-theme="light"] nav{background:rgba(240,244,255,.96)}
.nav-inner{display:flex;align-items:center;justify-content:space-between;height:64px}
.logo{display:flex;align-items:center;gap:10px;text-decoration:none}
.logo-icon{width:38px;height:38px;background:linear-gradient(135deg,#1d4ed8,#3b82f6);border-radius:10px;display:flex;align-items:center;justify-content:center;font-family:'Cormorant Garamond',serif;font-size:20px;font-weight:700;color:#fff;box-shadow:0 4px 16px rgba(59,130,246,.4)}
.logo-text{font-family:'Cormorant Garamond',serif;font-size:17px;font-weight:700;line-height:1.2}
.logo-text .w1{color:var(--blue2)}
.logo-text .w2{color:var(--text2);font-size:11px;font-weight:400;letter-spacing:.5px;text-transform:uppercase}
.nav-links{display:flex;align-items:center;gap:20px}
.nav-links a{color:var(--text2);font-size:13px;text-decoration:none;transition:color .2s;font-weight:400}
.nav-links a:hover{color:var(--blue2)}
.nav-right{display:flex;align-items:center;gap:8px}
.theme-btn{width:34px;height:34px;border-radius:50%;background:var(--bg3);border:1px solid var(--border);cursor:pointer;font-size:14px;display:flex;align-items:center;justify-content:center;transition:all .2s;color:var(--text)}
.theme-btn:hover{border-color:var(--blue);box-shadow:0 0 10px rgba(59,130,246,.3)}
.nav-wa{background:var(--green);color:#fff;border:none;padding:7px 14px;border-radius:18px;font-size:12px;cursor:pointer;font-weight:600;text-decoration:none;display:inline-block;font-family:'Outfit',sans-serif;transition:all .2s}
.nav-wa:hover{opacity:.88}
.hamburger{display:none;flex-direction:column;gap:5px;cursor:pointer;background:none;border:none;padding:4px}
.hamburger span{display:block;width:22px;height:1.5px;background:var(--text2);border-radius:2px}
.mobile-menu{display:none;flex-direction:column;background:var(--bg2);border-top:1px solid var(--border);padding:14px 5%}
.mobile-menu.open{display:flex}
.mobile-menu a{color:var(--text2);font-size:14px;text-decoration:none;padding:11px 0;border-bottom:.5px solid var(--border)}
.mobile-menu a:last-child{border:none}

/* ── STUDENTS BANNER ── */
.students-banner{background:var(--bg2);border-bottom:1px solid var(--border);padding:9px 5%;display:flex;align-items:center;gap:12px;flex-wrap:wrap;overflow:hidden}
.sb-label{font-size:11px;color:var(--text3);text-transform:uppercase;letter-spacing:.8px;white-space:nowrap}
.sb-names{display:flex;gap:8px;flex-wrap:wrap}
.sb-name{display:flex;align-items:center;gap:6px;background:var(--bg3);border:1px solid var(--border2);border-radius:20px;padding:4px 12px;font-size:12px;color:var(--text);font-weight:500;transition:all .2s}
.sb-name:hover{border-color:var(--blue);box-shadow:0 0 12px rgba(59,130,246,.2)}
.sb-avatar{width:20px;height:20px;border-radius:50%;background:linear-gradient(135deg,#1d4ed8,#3b82f6);display:flex;align-items:center;justify-content:center;font-size:9px;font-weight:700;color:#fff;flex-shrink:0}
.dot-green{width:5px;height:5px;background:var(--green);border-radius:50%;display:inline-block;animation:blink 1.5s infinite;margin-left:4px}
@keyframes blink{0%,100%{opacity:1}50%{opacity:.2}}

/* ── LIMITED OFFER BANNER ── */
.offer-banner{background:linear-gradient(90deg,#1d4ed8,#7c3aed,#1d4ed8);background-size:200% 100%;animation:gradMove 4s linear infinite;padding:10px 5%;text-align:center;font-size:13px;font-weight:600;color:#fff;letter-spacing:.3px;cursor:pointer}
.offer-banner:hover{opacity:.92}
@keyframes gradMove{0%{background-position:0% 50%}100%{background-position:200% 50%}}
.offer-banner span{background:rgba(255,255,255,.2);padding:2px 10px;border-radius:10px;margin:0 6px;font-size:11px;letter-spacing:.5px}

/* ── HERO ── */
#home{padding:84px 5% 68px;text-align:center;background:var(--bg2);position:relative;overflow:hidden}
.hero-orb1{position:absolute;top:-20%;left:-10%;width:60%;height:80%;background:radial-gradient(ellipse,rgba(59,130,246,.1),transparent 65%);pointer-events:none}
.hero-orb2{position:absolute;bottom:-20%;right:-10%;width:50%;height:70%;background:radial-gradient(ellipse,rgba(168,85,247,.07),transparent 65%);pointer-events:none}
.hero-grid{position:absolute;inset:0;background-image:linear-gradient(rgba(59,130,246,.06) 1px,transparent 1px),linear-gradient(90deg,rgba(59,130,246,.06) 1px,transparent 1px);background-size:44px 44px;pointer-events:none}
.hero-badge{display:inline-flex;align-items:center;gap:8px;background:rgba(59,130,246,.1);border:1px solid rgba(59,130,246,.3);color:var(--blue2);font-size:11px;padding:6px 16px;border-radius:20px;margin-bottom:22px;letter-spacing:.8px;text-transform:uppercase;font-weight:600;position:relative}
.dot-live{width:6px;height:6px;background:var(--green);border-radius:50%;animation:pulse 1.5s infinite}
@keyframes pulse{0%,100%{opacity:1;transform:scale(1)}50%{opacity:.3;transform:scale(.75)}}
.hero-h1{font-family:'Cormorant Garamond',serif;font-size:clamp(32px,5.5vw,58px);font-weight:600;line-height:1.18;margin-bottom:14px;position:relative;letter-spacing:-.5px}
.hero-h1 em{background:linear-gradient(135deg,var(--blue2),#a78bfa);-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;font-style:normal}
.hero-sub{color:var(--text2);font-size:15px;margin-bottom:8px;font-weight:300}
.hero-world{color:var(--text3);font-size:13px;margin-bottom:34px}
.hero-btns{display:flex;gap:12px;justify-content:center;flex-wrap:wrap;position:relative}
.btn-blue{background:linear-gradient(135deg,#1d4ed8,#3b82f6);color:#fff;border:none;padding:13px 28px;border-radius:28px;font-size:14px;font-weight:700;cursor:pointer;transition:all .2s;font-family:'Outfit',sans-serif;box-shadow:0 6px 20px rgba(59,130,246,.35)}
.btn-blue:hover{transform:translateY(-2px);box-shadow:0 10px 28px rgba(59,130,246,.45)}
.btn-outline{background:transparent;color:var(--text);border:1px solid var(--border2);padding:13px 22px;border-radius:28px;font-size:14px;cursor:pointer;font-family:'Outfit',sans-serif;transition:all .2s;text-decoration:none;display:inline-flex;align-items:center}
.btn-outline:hover{border-color:var(--blue);color:var(--blue2);box-shadow:0 0 16px rgba(59,130,246,.2)}

/* ── TRUST ── */
.trust-bar{background:var(--bg3);padding:12px 5%;display:flex;align-items:center;justify-content:center;gap:24px;flex-wrap:wrap;border-top:1px solid var(--border);border-bottom:1px solid var(--border)}
.trust-item{font-size:12px;color:var(--text2);white-space:nowrap}

/* ── COUNTDOWN ── */
#countdown-section{background:var(--bg);padding:60px 5%}
.countdown-wrap{background:var(--bg2);border:1px solid var(--border2);border-radius:20px;padding:36px;text-align:center;max-width:660px;margin:0 auto;position:relative;overflow:hidden}
.countdown-wrap::before{content:'';position:absolute;top:0;left:50%;transform:translateX(-50%);width:80%;height:1px;background:linear-gradient(90deg,transparent,var(--blue),transparent)}
.countdown-wrap::after{content:'';position:absolute;inset:0;background:radial-gradient(ellipse at 50% -10%,rgba(59,130,246,.08),transparent 60%);pointer-events:none}
.cd-label{font-size:11px;color:var(--blue2);letter-spacing:1px;text-transform:uppercase;font-weight:600;margin-bottom:8px}
.cd-title{font-family:'Cormorant Garamond',serif;font-size:20px;font-weight:500;margin-bottom:22px;color:var(--text)}
.timer-boxes{display:flex;gap:12px;justify-content:center;flex-wrap:wrap;margin-bottom:22px}
.timer-unit{background:var(--bg3);border:1px solid var(--border2);border-radius:12px;padding:14px 20px;min-width:76px;position:relative;overflow:hidden}
.timer-unit::before{content:'';position:absolute;top:0;left:0;right:0;height:1px;background:linear-gradient(90deg,transparent,var(--blue2),transparent)}
.timer-num{font-family:'Cormorant Garamond',serif;font-size:40px;font-weight:700;color:var(--blue2);line-height:1;display:block}
.timer-lbl{font-size:10px;color:var(--text2);letter-spacing:1px;text-transform:uppercase;margin-top:4px;display:block}
.class-badge{display:inline-flex;align-items:center;gap:7px;background:rgba(34,197,94,.1);border:1px solid rgba(34,197,94,.25);color:var(--green);padding:8px 18px;border-radius:18px;font-size:13px;font-weight:500}
.class-badge.off{background:rgba(239,68,68,.1);border-color:rgba(239,68,68,.25);color:var(--red)}

/* ── SECTIONS ── */
section{padding:64px 5%}
.sec-head{text-align:center;margin-bottom:42px}
.sec-head h2{font-family:'Cormorant Garamond',serif;font-size:clamp(24px,4vw,38px);font-weight:600;color:var(--text);margin-bottom:8px;letter-spacing:-.3px}
.sec-head p{color:var(--text2);font-size:13px;font-weight:300}
.blue-bar{display:inline-block;width:48px;height:2px;background:linear-gradient(90deg,transparent,var(--blue),transparent);border-radius:2px;margin:10px 0 0}

/* ── COURSES ── */
#courses{background:var(--bg2)}
.courses-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:16px}
.c-card{background:var(--bg3);border:1px solid var(--border);border-radius:18px;padding:28px 22px;text-align:center;position:relative;transition:all .28s;overflow:hidden}
.c-card::before{content:'';position:absolute;top:0;left:0;right:0;height:1px;background:linear-gradient(90deg,transparent,var(--border2),transparent);opacity:0;transition:opacity .3s}
.c-card:hover{transform:translateY(-6px);border-color:var(--border2);box-shadow:0 20px 48px rgba(59,130,246,.15)}
.c-card:hover::before{opacity:1}
.c-card.featured{border:1.5px solid var(--blue);box-shadow:0 0 28px rgba(59,130,246,.15)}
.feat-tag{position:absolute;top:-1px;left:50%;transform:translateX(-50%);background:linear-gradient(135deg,#1d4ed8,#3b82f6);color:#fff;font-size:10px;font-weight:700;padding:4px 14px;border-radius:0 0 10px 10px;white-space:nowrap;letter-spacing:.4px}
.c-emoji{font-size:38px;margin-bottom:14px;display:block}
.c-card h3{font-family:'Cormorant Garamond',serif;font-size:21px;font-weight:600;margin-bottom:8px;color:var(--text)}
.c-card p{font-size:12px;color:var(--text2);margin-bottom:6px;line-height:1.65;font-weight:300}
.grammar-topics{background:var(--bg4);border:1px solid var(--border);border-radius:10px;padding:10px 12px;margin:10px 0 14px;text-align:left}
.grammar-topic{font-size:11px;color:var(--text2);padding:3px 0;display:flex;align-items:center;gap:6px}
.grammar-topic::before{content:'';width:5px;height:5px;background:var(--blue2);border-radius:50%;flex-shrink:0}
.c-price{font-family:'Cormorant Garamond',serif;font-size:28px;font-weight:700;color:var(--gold);margin:0 0 14px;display:block}
.c-btn{background:linear-gradient(135deg,#1d4ed8,#3b82f6);color:#fff;border:none;padding:9px 22px;border-radius:20px;font-size:12px;cursor:pointer;font-weight:700;font-family:'Outfit',sans-serif;transition:all .2s;box-shadow:0 4px 12px rgba(59,130,246,.3)}
.c-btn:hover{transform:scale(1.04);box-shadow:0 6px 18px rgba(59,130,246,.4)}

/* ── LIVE ── */
#live{background:var(--bg)}
.live-box{background:var(--bg2);border:1px solid var(--border2);border-radius:20px;padding:28px;position:relative;overflow:hidden}
.live-box::before{content:'';position:absolute;top:0;left:0;right:0;height:1px;background:linear-gradient(90deg,transparent,var(--blue),transparent)}
.live-header{display:flex;align-items:center;justify-content:space-between;flex-wrap:wrap;gap:12px;margin-bottom:22px}
.live-title{display:flex;align-items:center;gap:9px}
.live-dot{width:10px;height:10px;background:var(--red);border-radius:50%;animation:blink .9s infinite;box-shadow:0 0 8px var(--red)}
.live-label{font-family:'Cormorant Garamond',serif;font-size:20px;font-weight:600}
.join-btn{background:linear-gradient(135deg,#16a34a,#22c55e);color:#fff;border:none;padding:10px 20px;border-radius:20px;font-size:13px;cursor:pointer;font-weight:600;font-family:'Outfit',sans-serif;text-decoration:none;display:inline-block;transition:all .2s;box-shadow:0 4px 12px rgba(34,197,94,.3)}
.join-btn:hover{opacity:.88;transform:translateY(-1px)}
.schedule-list{display:flex;flex-direction:column;gap:9px}
.sch-item{display:flex;align-items:center;justify-content:space-between;background:var(--bg3);border-radius:12px;padding:13px 16px;border:1px solid var(--border);transition:all .2s}
.sch-item:hover{border-color:var(--border2);box-shadow:0 4px 12px rgba(59,130,246,.1)}
.sch-left{display:flex;align-items:center;gap:9px}
.sch-dot{width:7px;height:7px;border-radius:50%;flex-shrink:0}
.sch-name{font-size:13px;font-weight:400}
.sch-right{display:flex;align-items:center;gap:9px}
.sch-time{color:var(--blue2);font-family:'Cormorant Garamond',serif;font-size:17px;font-weight:600}
.sch-pill{font-size:10px;padding:3px 10px;border-radius:7px;font-weight:700;letter-spacing:.4px}
.pill-live{background:rgba(239,68,68,.14);color:var(--red);border:1px solid rgba(239,68,68,.2)}
.pill-soon{background:rgba(59,130,246,.12);color:var(--blue2);border:1px solid rgba(59,130,246,.2)}
.wa-note{margin-top:16px;background:rgba(34,197,94,.07);border:1px solid rgba(34,197,94,.18);border-radius:11px;padding:13px 16px;font-size:13px;color:var(--text2);line-height:1.6}
.wa-note strong{color:var(--green)}

/* ── FAQ ── */
#faq{background:var(--bg2)}
.faq-list{max-width:720px;margin:0 auto;display:flex;flex-direction:column;gap:8px}
.faq-item{background:var(--bg3);border:1px solid var(--border);border-radius:14px;overflow:hidden;transition:all .2s}
.faq-item.open{border-color:var(--border2);box-shadow:0 4px 16px rgba(59,130,246,.1)}
.faq-q{display:flex;align-items:center;justify-content:space-between;padding:16px 18px;cursor:pointer;font-size:14px;font-weight:500;color:var(--text);gap:12px;user-select:none}
.faq-q:hover{color:var(--blue2)}
.faq-arrow{font-size:20px;color:var(--blue2);transition:transform .3s;flex-shrink:0}
.faq-item.open .faq-arrow{transform:rotate(45deg)}
.faq-a{max-height:0;overflow:hidden;transition:max-height .35s ease}
.faq-a-inner{padding:0 18px 16px;font-size:13px;color:var(--text2);line-height:1.8;font-weight:300}
.faq-item.open .faq-a{max-height:240px}

/* ── CEO ── */
#about{background:var(--bg)}
.ceo-card{background:var(--bg2);border:1px solid var(--border2);border-radius:20px;padding:34px;display:flex;align-items:flex-start;gap:26px;flex-wrap:wrap;position:relative;overflow:hidden}
.ceo-card::before{content:'';position:absolute;top:0;left:0;right:0;height:1px;background:linear-gradient(90deg,transparent,var(--blue),transparent)}
.ceo-card::after{content:'';position:absolute;top:0;right:0;width:45%;height:100%;background:radial-gradient(ellipse at right,rgba(59,130,246,.07),transparent 70%);pointer-events:none}
.ceo-photo{width:92px;height:92px;border-radius:50%;background:linear-gradient(135deg,#1d4ed8,#3b82f6);display:flex;align-items:center;justify-content:center;font-family:'Cormorant Garamond',serif;font-size:32px;font-weight:700;color:#fff;flex-shrink:0;border:2px solid var(--border2);position:relative;z-index:1;box-shadow:0 8px 24px rgba(59,130,246,.3)}
.ceo-info{position:relative;z-index:1;flex:1;min-width:200px}
.ceo-info h3{font-family:'Cormorant Garamond',serif;font-size:26px;font-weight:600;margin-bottom:3px}
.ceo-role{color:var(--blue2);font-size:11px;font-weight:600;letter-spacing:.8px;margin-bottom:12px;text-transform:uppercase}
.ceo-bio{font-size:13px;color:var(--text2);line-height:1.8;margin-bottom:14px;font-weight:300;max-width:500px}
.ceo-contact a{color:var(--green);font-size:13px;text-decoration:none;font-weight:500}
.ceo-contact a:hover{text-decoration:underline}

/* ── GOOGLE FORM ── */
#gform{background:var(--bg2)}
.gform-wrap{background:var(--bg3);border:1px solid var(--border2);border-radius:20px;padding:32px;max-width:700px;margin:0 auto;text-align:center;position:relative;overflow:hidden}
.gform-wrap::before{content:'';position:absolute;top:0;left:0;right:0;height:1px;background:linear-gradient(90deg,transparent,var(--blue),transparent)}
.gform-wrap h3{font-family:'Cormorant Garamond',serif;font-size:24px;font-weight:600;margin-bottom:6px}
.gform-wrap p{color:var(--text2);font-size:13px;margin-bottom:22px;font-weight:300;line-height:1.7}
.gform-note{background:rgba(59,130,246,.08);border:1px solid rgba(59,130,246,.2);border-radius:10px;padding:12px 16px;font-size:12px;color:var(--text2);margin-bottom:20px;line-height:1.7;text-align:left}
.gform-note strong{color:var(--blue2)}
.gform-btn{display:inline-flex;align-items:center;gap:8px;background:linear-gradient(135deg,#1d4ed8,#3b82f6);color:#fff;border:none;padding:14px 32px;border-radius:28px;font-size:15px;font-weight:700;cursor:pointer;font-family:'Outfit',sans-serif;transition:all .2s;text-decoration:none;box-shadow:0 6px 20px rgba(59,130,246,.35)}
.gform-btn:hover{transform:translateY(-2px);box-shadow:0 10px 28px rgba(59,130,246,.45)}

/* ── ENROLL ── */
#enroll{background:var(--bg)}
.flow-steps{display:flex;margin-bottom:32px;overflow-x:auto;padding:4px 0;max-width:700px;margin-left:auto;margin-right:auto}
.flow-step{flex:1;min-width:120px;text-align:center;position:relative}
.flow-step:not(:last-child)::after{content:'';position:absolute;top:16px;left:58%;right:-10%;height:1px;background:linear-gradient(90deg,var(--blue),var(--border));z-index:0}
.step-circle{width:32px;height:32px;border-radius:50%;background:linear-gradient(135deg,#1d4ed8,#3b82f6);color:#fff;font-weight:700;font-size:13px;display:flex;align-items:center;justify-content:center;margin:0 auto 7px;position:relative;z-index:1;box-shadow:0 4px 10px rgba(59,130,246,.3)}
.step-label{font-size:11px;color:var(--text2);line-height:1.4}
.pay-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(175px,1fr));gap:12px;margin-bottom:24px}
.pay-card{background:var(--bg2);border:1px solid var(--border);border-radius:14px;padding:18px;transition:all .2s}
.pay-card:hover{border-color:var(--border2);box-shadow:0 6px 18px rgba(59,130,246,.1)}
.pay-card h4{font-size:11px;color:var(--text2);font-weight:500;margin-bottom:7px;letter-spacing:.4px;text-transform:uppercase}
.pay-num{font-family:'Cormorant Garamond',serif;font-size:16px;font-weight:700;color:var(--gold);letter-spacing:.3px;margin-bottom:3px;word-break:break-all}
.pay-note{font-size:11px;color:var(--text3);line-height:1.5}
.form-box{background:var(--bg2);border:1px solid var(--border2);border-radius:20px;padding:30px;position:relative;overflow:hidden}
.form-box::before{content:'';position:absolute;top:0;left:0;right:0;height:1px;background:linear-gradient(90deg,transparent,var(--blue),transparent)}
.form-box h3{font-family:'Cormorant Garamond',serif;font-size:23px;font-weight:600;margin-bottom:4px}
.form-box .fsub{font-size:13px;color:var(--text2);margin-bottom:20px;font-weight:300}
.pay-info-box{background:rgba(59,130,246,.07);border:1px solid rgba(59,130,246,.2);border-radius:10px;padding:12px 14px;font-size:12px;color:var(--text2);margin-bottom:15px;line-height:1.7}
.pay-info-box strong{color:var(--blue2)}
.f-grid{display:grid;grid-template-columns:1fr 1fr;gap:9px;margin-bottom:9px}
.f-full{margin-bottom:9px}
input,select,textarea{width:100%;padding:11px 14px;background:var(--bg);border:1px solid var(--border);border-radius:9px;color:var(--text);font-size:13px;font-family:'Outfit',sans-serif;outline:none;transition:all .2s}
input:focus,select:focus,textarea:focus{border-color:var(--blue);box-shadow:0 0 0 3px rgba(59,130,246,.1)}
input::placeholder,textarea::placeholder{color:var(--text3)}
select option{background:var(--bg2)}
textarea{resize:vertical;min-height:68px}
.pay-methods-label{font-size:12px;color:var(--text2);margin:11px 0 7px}
.pay-pills{display:flex;gap:7px;flex-wrap:wrap;margin-bottom:18px}
.ppill{background:var(--bg);border:1px solid var(--border);border-radius:18px;padding:7px 15px;font-size:12px;color:var(--text2);cursor:pointer;transition:all .2s;font-family:'Outfit',sans-serif}
.ppill.active{border-color:var(--blue);color:var(--blue2);background:var(--blue-glow)}
.submit-btn{width:100%;background:linear-gradient(135deg,#1d4ed8,#3b82f6);color:#fff;border:none;padding:15px;border-radius:28px;font-size:15px;font-weight:700;cursor:pointer;font-family:'Outfit',sans-serif;transition:all .2s;box-shadow:0 6px 20px rgba(59,130,246,.3)}
.submit-btn:hover{transform:translateY(-2px);box-shadow:0 10px 28px rgba(59,130,246,.4)}
.or-line{text-align:center;color:var(--text3);font-size:12px;margin:14px 0;position:relative}
.or-line::before,.or-line::after{content:'';position:absolute;top:50%;width:40%;height:.5px;background:var(--border)}
.or-line::before{left:0}.or-line::after{right:0}
.wa-big-btn{width:100%;background:linear-gradient(135deg,#16a34a,#22c55e);color:#fff;border:none;padding:14px;border-radius:28px;font-size:14px;font-weight:700;cursor:pointer;font-family:'Outfit',sans-serif;transition:all .2s;text-decoration:none;display:block;text-align:center;box-shadow:0 6px 16px rgba(34,197,94,.25)}
.wa-big-btn:hover{transform:translateY(-2px);box-shadow:0 10px 24px rgba(34,197,94,.35)}

/* ── SEC BAR ── */
.sec-bar{background:var(--bg3);padding:12px 5%;display:flex;align-items:center;justify-content:center;gap:22px;flex-wrap:wrap;border-top:1px solid var(--border)}
.sec-item{font-size:11px;color:var(--text3)}

/* ── FOOTER ── */
footer{background:var(--bg);padding:44px 5% 26px;border-top:1px solid var(--border)}
.footer-inner{display:flex;flex-wrap:wrap;gap:32px;justify-content:space-between;margin-bottom:26px}
.footer-brand p{font-size:13px;color:var(--text3);margin-top:9px;max-width:210px;line-height:1.7;font-weight:300}
.footer-col h4{font-size:11px;color:var(--text3);letter-spacing:.8px;text-transform:uppercase;margin-bottom:11px;font-weight:500}
.footer-col a{display:block;color:var(--text2);font-size:13px;text-decoration:none;margin-bottom:7px;transition:color .2s;font-weight:300}
.footer-col a:hover{color:var(--blue2)}
.footer-bottom{border-top:1px solid var(--border);padding-top:18px;display:flex;align-items:center;justify-content:space-between;flex-wrap:wrap;gap:8px}
.footer-copy{font-size:11px;color:var(--text3)}

/* ── POPUP ── */
.popup-overlay{display:none;position:fixed;top:0;left:0;right:0;bottom:0;background:rgba(0,0,0,.82);z-index:999;align-items:center;justify-content:center;backdrop-filter:blur(8px)}
.popup-overlay.show{display:flex}
.popup{background:var(--bg2);border:1px solid var(--border2);border-radius:24px;padding:34px 26px;text-align:center;max-width:400px;width:92%;animation:popIn .32s cubic-bezier(.34,1.56,.64,1);position:relative;overflow:hidden}
.popup::before{content:'';position:absolute;top:0;left:0;right:0;height:1px;background:linear-gradient(90deg,transparent,var(--blue),transparent)}
@keyframes popIn{from{transform:scale(.8);opacity:0}to{transform:scale(1);opacity:1}}
.popup-icon{font-size:48px;margin-bottom:13px}
.popup h3{font-family:'Cormorant Garamond',serif;font-size:24px;margin-bottom:8px;font-weight:600}
.popup p{font-size:13px;color:var(--text2);line-height:1.7;margin-bottom:16px;font-weight:300}
.popup-steps{background:var(--bg3);border-radius:11px;padding:14px;margin-bottom:16px;text-align:left}
.popup-step{display:flex;gap:10px;align-items:flex-start;margin-bottom:9px;font-size:12px;color:var(--text2)}
.popup-step:last-child{margin:0}
.ps-num{width:19px;height:19px;border-radius:50%;background:linear-gradient(135deg,#1d4ed8,#3b82f6);color:#fff;font-size:10px;font-weight:700;display:flex;align-items:center;justify-content:center;flex-shrink:0;margin-top:1px}
.popup-close{background:linear-gradient(135deg,#1d4ed8,#3b82f6);color:#fff;border:none;padding:11px 26px;border-radius:20px;font-size:14px;font-weight:700;cursor:pointer;font-family:'Outfit',sans-serif;box-shadow:0 4px 12px rgba(59,130,246,.3)}
.popup-close:hover{opacity:.88}

/* ── FADE ── */
.fade-in{opacity:0;transform:translateY(22px);transition:opacity .6s ease,transform .6s ease}
.fade-in.visible{opacity:1;transform:translateY(0)}

/* ── RESPONSIVE ── */
@media(max-width:640px){
  .nav-links{display:none}
  .hamburger{display:flex}
  .f-grid{grid-template-columns:1fr}
  .footer-inner{flex-direction:column;gap:18px}
  .trust-bar .trust-item:nth-child(n+4){display:none}
  .ceo-card{flex-direction:column}
  .flow-step:not(:last-child)::after{display:none}
}
@media(max-width:480px){
  .timer-unit{min-width:62px;padding:11px 13px}
  .timer-num{font-size:32px}
}
</style>
</head>
<body>

<!-- LIMITED OFFER BANNER -->
<div class="offer-banner" onclick="document.getElementById('enroll').scrollIntoView({behavior:'smooth'})">
  🔥 LIMITED OFFER <span>ENDING SOON</span> — Enroll Now &amp; Get Your <strong>First Course Absolutely FREE!</strong> &nbsp;→ Click to Enroll
</div>

<!-- NAV -->
<nav>
  <div class="nav-inner">
    <a href="#home" class="logo">
      <div class="logo-icon">W</div>
      <div class="logo-text">
        <div class="w1">WisdomWave</div>
        <div class="w2">Learning Institute</div>
      </div>
    </a>
    <div class="nav-links">
      <a href="#home">Home</a>
      <a href="#courses">Courses</a>
      <a href="#live">Live Classes</a>
      <a href="#gform">Google Form</a>
      <a href="#faq">FAQ</a>
      <a href="#about">About</a>
      <a href="#enroll">Enroll</a>
    </div>
    <div class="nav-right">
      <button class="theme-btn" onclick="toggleTheme()" id="themeBtn">🌙</button>
      <a href="https://wa.me/923018573005" target="_blank" class="nav-wa">💬 WhatsApp</a>
    </div>
    <button class="hamburger" onclick="toggleMenu()" aria-label="Menu">
      <span></span><span></span><span></span>
    </button>
  </div>
  <div class="mobile-menu" id="mobileMenu">
    <a href="#home" onclick="closeMenu()">Home</a>
    <a href="#courses" onclick="closeMenu()">Courses</a>
    <a href="#live" onclick="closeMenu()">Live Classes</a>
    <a href="#gform" onclick="closeMenu()">Google Form</a>
    <a href="#faq" onclick="closeMenu()">FAQ</a>
    <a href="#about" onclick="closeMenu()">About</a>
    <a href="#enroll" onclick="closeMenu()">Enroll Now</a>
    <a href="https://wa.me/923018573005" target="_blank">📱 WhatsApp: 03018573005</a>
  </div>
</nav>

<!-- STUDENTS BANNER -->
<div class="students-banner">
  <div class="sb-label">Our Students</div>
  <div class="sb-names">
    <div class="sb-name"><div class="sb-avatar">HK</div>Haris Khan<span class="dot-green"></span></div>
    <div class="sb-name"><div class="sb-avatar">HZ</div>Huzaifa<span class="dot-green"></span></div>
    <div class="sb-name"><div class="sb-avatar">IN</div>Inam<span class="dot-green"></span></div>
    <div class="sb-name"><div class="sb-avatar">ZB</div>Zaib<span class="dot-green"></span></div>
  </div>
</div>

<!-- HERO -->
<section id="home">
  <div class="hero-orb1"></div>
  <div class="hero-orb2"></div>
  <div class="hero-grid"></div>
  <div class="hero-badge"><span class="dot-live"></span> Live Classes Daily — 5:00 PM</div>
  <h1 class="hero-h1">Learn <em>English &amp; Computer</em><br>Skills Online</h1>
  <p class="hero-sub">Professional live classes — Expert teachers, real results, affordable fees</p>
  <p class="hero-world">🌍 Students from Pakistan, UAE, Saudi Arabia, UK &amp; worldwide</p>
  <div class="hero-btns">
    <button class="btn-blue" onclick="document.getElementById('enroll').scrollIntoView({behavior:'smooth'})">🎓 Enroll Now — First Course FREE</button>
    <a href="https://wa.me/923018573005?text=Hello!%20I%20want%20to%20know%20more%20about%20WisdomWave%20Learning%20Institute." target="_blank" class="btn-outline">💬 Ask on WhatsApp</a>
  </div>
</section>

<!-- TRUST BAR -->
<div class="trust-bar">
  <div class="trust-item">✅ Verified Institute</div>
  <div class="trust-item">🔒 Secure Payments</div>
  <div class="trust-item">🌐 Global Students</div>
  <div class="trust-item">📜 Certificate Provided</div>
  <div class="trust-item">💬 WhatsApp Support 24/7</div>
  <div class="trust-item">🆓 First Course FREE</div>
</div>

<!-- COUNTDOWN -->
<section id="countdown-section">
  <div class="sec-head fade-in">
    <h2>Next Live Class</h2>
    <div class="blue-bar"></div>
    <p style="margin-top:9px">Daily at 5:00 PM — Don't miss it!</p>
  </div>
  <div class="countdown-wrap fade-in">
    <div class="cd-label">⏳ Class Starts In</div>
    <div class="cd-title">Spoken English — Beginner Level</div>
    <div class="timer-boxes">
      <div class="timer-unit"><span class="timer-num" id="t-hours">00</span><span class="timer-lbl">Hours</span></div>
      <div class="timer-unit"><span class="timer-num" id="t-mins">00</span><span class="timer-lbl">Minutes</span></div>
      <div class="timer-unit"><span class="timer-num" id="t-secs">00</span><span class="timer-lbl">Seconds</span></div>
    </div>
    <div id="classBadge" class="class-badge">
      <span class="dot-live"></span>&nbsp;<span id="classTxt">Calculating...</span>
    </div>
  </div>
</section>

<!-- COURSES -->
<section id="courses">
  <div class="sec-head fade-in">
    <h2>Our Courses</h2>
    <div class="blue-bar"></div>
    <p style="margin-top:9px">Rs. 2000/month — Professional learning for everyone</p>
  </div>
  <div class="courses-grid">

    <!-- SPOKEN ENGLISH -->
    <div class="c-card fade-in">
      <span class="c-emoji">🗣️</span>
      <h3>Spoken English</h3>
      <p>Basic to advanced communication. Speak confidently in any situation.</p>
      <span class="c-price">Rs. 2000/month</span>
      <button class="c-btn" onclick="enrollFor('Spoken English')">Enroll Now</button>
    </div>

    <!-- ENGLISH GRAMMAR -->
    <div class="c-card featured fade-in">
      <div class="feat-tag">⭐ Special Class</div>
      <span class="c-emoji">📖</span>
      <h3>English Grammar</h3>
      <p>Complete grammar course — from basics to advanced level.</p>
      <div class="grammar-topics">
        <div class="grammar-topic">Parts of Speech</div>
        <div class="grammar-topic">Tenses</div>
        <div class="grammar-topic">Passive Voice</div>
        <div class="grammar-topic">Direct &amp; Indirect Speech</div>
        <div class="grammar-topic">Clause</div>
        <div class="grammar-topic">Sentence Structure</div>
      </div>
      <span class="c-price">Rs. 2000/month</span>
      <button class="c-btn" onclick="enrollFor('English Grammar')">Enroll Now</button>
    </div>

    <!-- FULL PACKAGE -->
    <div class="c-card fade-in">
      <span class="c-emoji">💡</span>
      <h3>Full Package</h3>
      <p>Spoken English + Grammar both. Best value for complete English mastery.</p>
      <span class="c-price">Rs. 2000/month</span>
      <button class="c-btn" onclick="enrollFor('Full Package')">Enroll Now</button>
    </div>

  </div>

  <!-- FREE OFFER NOTE -->
  <div style="margin-top:20px;background:rgba(59,130,246,.08);border:1px solid rgba(59,130,246,.25);border-radius:14px;padding:18px 22px;text-align:center" class="fade-in">
    <p style="font-size:14px;font-weight:600;color:var(--blue2);margin-bottom:4px">🎁 LIMITED OFFER — First Course Absolutely FREE!</p>
    <p style="font-size:13px;color:var(--text2);font-weight:300">Enroll now and attend your first complete course without paying anything. Limited seats available.</p>
  </div>
</section>

<!-- LIVE CLASSES -->
<section id="live">
  <div class="sec-head fade-in">
    <h2>Live Classes</h2>
    <div class="blue-bar"></div>
    <p style="margin-top:9px">Join live every day — interactive, real-time learning</p>
  </div>
  <div class="live-box fade-in">
    <div class="live-header">
      <div class="live-title">
        <div class="live-dot"></div>
        <div class="live-label">Today's Schedule</div>
      </div>
      <a href="https://wa.me/923018573005?text=Hello!%20I%20want%20to%20join%20today's%20live%20class%20at%205:00%20PM." target="_blank" class="join-btn">📱 Join via WhatsApp</a>
    </div>
    <div class="schedule-list">
      <div class="sch-item">
        <div class="sch-left"><div class="sch-dot" style="background:var(--green);box-shadow:0 0 6px var(--green)"></div><div class="sch-name">Spoken English — Beginner Level</div></div>
        <div class="sch-right"><div class="sch-time">5:00 PM</div><div class="sch-pill pill-live">LIVE</div></div>
      </div>
      <div class="sch-item">
        <div class="sch-left"><div class="sch-dot" style="background:var(--blue2);box-shadow:0 0 6px var(--blue2)"></div><div class="sch-name">English Grammar — Parts of Speech &amp; Tenses</div></div>
        <div class="sch-right"><div class="sch-time">6:00 PM</div><div class="sch-pill pill-soon">UPCOMING</div></div>
      </div>
      <div class="sch-item">
        <div class="sch-left"><div class="sch-dot" style="background:var(--text3)"></div><div class="sch-name">Advanced English — Speaking Practice</div></div>
        <div class="sch-right"><div class="sch-time">7:00 PM</div><div class="sch-pill pill-soon">UPCOMING</div></div>
      </div>
    </div>
    <div class="wa-note">
      📱 Classes via <strong>WhatsApp Video Call</strong> — After enrollment you will be added to our WhatsApp group. Class link is sent daily at <strong>4:45 PM</strong>.
    </div>
  </div>
</section>

<!-- GOOGLE FORM -->
<section id="gform">
  <div class="sec-head fade-in">
    <h2>Enroll via Google Form</h2>
    <div class="blue-bar"></div>
    <p style="margin-top:9px">Fill our official Google Form to register</p>
  </div>
  <div class="gform-wrap fade-in">
    <h3>📋 Official Enrollment Form</h3>
    <p>Click the button below to open our Google Form. Fill in your details and submit — we will contact you within 2 hours to confirm your seat.</p>
    <div class="gform-note">
      <strong>📌 How to add your Google Form link:</strong><br>
      1. Go to <strong>forms.google.com</strong> → Create a new form<br>
      2. Add fields: Name, Phone, City, Course, Message<br>
      3. Click "Send" → Copy the link<br>
      4. Replace the link in the button below (WhatsApp us: <strong>03018573005</strong>)
    </div>
    <a href="https://forms.google.com" target="_blank" class="gform-btn">
      📋 Open Enrollment Google Form
    </a>
    <p style="margin-top:14px;font-size:12px;color:var(--text3)">Or fill the form directly on this page below ↓</p>
  </div>
</section>

<!-- FAQ -->
<section id="faq">
  <div class="sec-head fade-in">
    <h2>Frequently Asked Questions</h2>
    <div class="blue-bar"></div>
    <p style="margin-top:9px">Answers to common questions</p>
  </div>
  <div class="faq-list fade-in">
    <div class="faq-item">
      <div class="faq-q" onclick="toggleFaq(this)">How do classes work?<span class="faq-arrow">+</span></div>
      <div class="faq-a"><div class="faq-a-inner">Classes are held via <strong>WhatsApp Video Call</strong>. After enrollment you'll be added to our group. A class link is sent every day at <strong>4:45 PM</strong>. No extra app needed — just WhatsApp!</div></div>
    </div>
    <div class="faq-item">
      <div class="faq-q" onclick="toggleFaq(this)">How do I pay?<span class="faq-arrow">+</span></div>
      <div class="faq-a"><div class="faq-a-inner">Send <strong>Rs. 2000</strong> to EasyPaisa <strong>03018573005</strong> or Bank Account <strong>1644348071002307</strong>. Then send the payment screenshot to WhatsApp: <strong>03018573005</strong>. Confirmed within 2 hours!</div></div>
    </div>
    <div class="faq-item">
      <div class="faq-q" onclick="toggleFaq(this)">What is the Limited Offer — First Course FREE?<span class="faq-arrow">+</span></div>
      <div class="faq-a"><div class="faq-a-inner">New students who enroll now will get their <strong>first complete course absolutely FREE</strong>. This is a limited time offer with limited seats. Enroll now to secure your free course. WhatsApp: <strong>03018573005</strong></div></div>
    </div>
    <div class="faq-item">
      <div class="faq-q" onclick="toggleFaq(this)">What topics are covered in English Grammar?<span class="faq-arrow">+</span></div>
      <div class="faq-a"><div class="faq-a-inner">Our English Grammar course covers: <strong>Parts of Speech, Tenses, Passive Voice, Direct &amp; Indirect Speech, Clause, and Sentence Structure</strong>. Everything from basic to advanced level in a structured way.</div></div>
    </div>
    <div class="faq-item">
      <div class="faq-q" onclick="toggleFaq(this)">What if I miss a class?<span class="faq-arrow">+</span></div>
      <div class="faq-a"><div class="faq-a-inner">The missed class recording is shared in the WhatsApp group. Classes are daily so you can join again the next day.</div></div>
    </div>
    <div class="faq-item">
      <div class="faq-q" onclick="toggleFaq(this)">Will I get a certificate?<span class="faq-arrow">+</span></div>
      <div class="faq-a"><div class="faq-a-inner">Yes! A <strong>WisdomWave Learning Institute Certificate</strong> is given upon course completion. Available in digital and printed form.</div></div>
    </div>
    <div class="faq-item">
      <div class="faq-q" onclick="toggleFaq(this)">Can I join from UAE, UK or other countries?<span class="faq-arrow">+</span></div>
      <div class="faq-a"><div class="faq-a-inner">Absolutely! WhatsApp works globally. For international payment options contact: <strong>03018573005</strong></div></div>
    </div>
  </div>
</section>

<!-- CEO -->
<section id="about">
  <div class="sec-head fade-in">
    <h2>Founder &amp; CEO</h2>
    <div class="blue-bar"></div>
    <p style="margin-top:9px">The vision behind WisdomWave</p>
  </div>
  <div class="ceo-card fade-in">
    <div class="ceo-photo">AK</div>
    <div class="ceo-info">
      <h3>Amir Khan</h3>
      <div class="ceo-role">Founder &amp; CEO — WisdomWave Learning Institute</div>
      <p class="ceo-bio">My vision is simple — every student deserves quality education, regardless of where they live or their financial situation. WisdomWave Learning Institute was built so that no student anywhere in the world is left behind. Through live daily classes and affordable fees, we are changing lives one student at a time.</p>
      <div class="ceo-contact">
        <a href="https://wa.me/923018573005" target="_blank">📱 WhatsApp: 03018573005</a>
      </div>
    </div>
  </div>
</section>

<!-- ENROLL + PAYMENT -->
<section id="enroll">
  <div class="sec-head fade-in">
    <h2>Enroll Now</h2>
    <div class="blue-bar"></div>
    <p style="margin-top:9px">Fill the form — confirmed within 2 hours</p>
  </div>

  <div class="flow-steps fade-in">
    <div class="flow-step"><div class="step-circle">1</div><div class="step-label">Fill the Form</div></div>
    <div class="flow-step"><div class="step-circle">2</div><div class="step-label">Send Fee via EasyPaisa / Bank</div></div>
    <div class="flow-step"><div class="step-circle">3</div><div class="step-label">Send Screenshot to WhatsApp</div></div>
    <div class="flow-step"><div class="step-circle">✓</div><div class="step-label">Join Group &amp; Start!</div></div>
  </div>

  <div class="pay-grid fade-in">
    <div class="pay-card" style="border-color:rgba(34,197,94,.28)">
      <h4>✅ EasyPaisa</h4>
      <div class="pay-num">03018573005</div>
      <div class="pay-note">Send Rs. 2000 → screenshot to WhatsApp → confirmed in 2 hrs</div>
    </div>
    <div class="pay-card" style="border-color:rgba(59,130,246,.28)">
      <h4>🏦 Bank Account</h4>
      <div class="pay-num">1644348071002307</div>
      <div class="pay-note">Bank transfer — then send screenshot to WhatsApp</div>
    </div>
    <div class="pay-card" style="border-color:rgba(59,130,246,.2)">
      <h4>🏦 Bank IBAN</h4>
      <div class="pay-num" style="font-size:12px">PK65MUCB1644348071002307</div>
      <div class="pay-note">For international &amp; local bank transfers</div>
    </div>
    <div class="pay-card" style="border-color:rgba(37,211,102,.22)">
      <h4>💬 WhatsApp</h4>
      <div class="pay-num" style="color:#25d366">03018573005</div>
      <div class="pay-note">Any questions about payment — call or message</div>
    </div>
  </div>

  <div class="form-box fade-in">
    <h3>Student Enrollment Form</h3>
    <p class="fsub">Your details go directly to us on WhatsApp ✅</p>
    <div class="pay-info-box">
      💡 After submitting, send <strong>Rs. 2000</strong> to EasyPaisa <strong>03018573005</strong> or Bank <strong>1644348071002307</strong> → send screenshot to WhatsApp <strong>03018573005</strong> → done!
    </div>
    <div class="f-grid">
      <input type="text" id="fname" placeholder="Full Name *">
      <input type="tel" id="fphone" placeholder="Your WhatsApp Number *">
    </div>
    <div class="f-grid">
      <input type="text" id="fcity" placeholder="City / Country *">
      <input type="email" id="femail" placeholder="Email (optional)">
    </div>
    <div class="f-full">
      <select id="fcourse">
        <option value="">Select Course *</option>
        <option value="Spoken English">Spoken English — Rs. 2000/month</option>
        <option value="English Grammar">English Grammar (Special Class) — Rs. 2000/month</option>
        <option value="Full Package">Full Package (Spoken + Grammar) — Rs. 2000/month</option>
      </select>
    </div>
    <div class="f-full">
      <input type="text" id="ftxn" placeholder="Transaction ID (optional — or send later on WhatsApp)">
    </div>
    <div class="f-full">
      <textarea id="fnotes" placeholder="Any question or message (optional)..."></textarea>
    </div>
    <div class="pay-methods-label">Payment method:</div>
    <div class="pay-pills">
      <div class="ppill active" onclick="selectPay(this)">EasyPaisa</div>
      <div class="ppill" onclick="selectPay(this)">Bank Transfer</div>
      <div class="ppill" onclick="selectPay(this)">Pay Later</div>
    </div>
    <button class="submit-btn" onclick="submitEnroll()">🎓 Submit — Send to WhatsApp</button>
    <div class="or-line">or contact us directly</div>
    <a href="https://wa.me/923018573005?text=Hello!%20I%20want%20to%20enroll%20at%20WisdomWave%20Learning%20Institute." target="_blank" class="wa-big-btn">💬 WhatsApp: 03018573005</a>
  </div>
</section>

<!-- SEC BAR -->
<div class="sec-bar">
  <div class="sec-item">✅ Verified Institute</div>
  <div class="sec-item">🔒 Secure Payments</div>
  <div class="sec-item">🛡️ Data Protected</div>
  <div class="sec-item">🌐 Worldwide Access</div>
</div>

<!-- FOOTER -->
<footer>
  <div class="footer-inner">
    <div class="footer-brand">
      <div style="font-family:'Cormorant Garamond',serif;font-size:18px;font-weight:700;color:var(--blue2)">WisdomWave <span style="color:var(--text2);font-weight:400;font-size:14px">Learning Institute</span></div>
      <p>Professional online education for students worldwide. Quality learning at affordable prices.</p>
    </div>
    <div class="footer-col">
      <h4>Courses</h4>
      <a href="#courses">Spoken English</a>
      <a href="#courses">English Grammar</a>
      <a href="#courses">Full Package</a>
    </div>
    <div class="footer-col">
      <h4>Institute</h4>
      <a href="#live">Live Classes</a>
      <a href="#gform">Google Form</a>
      <a href="#faq">FAQ</a>
      <a href="#about">About CEO</a>
    </div>
    <div class="footer-col">
      <h4>Contact</h4>
      <a href="https://wa.me/923018573005" target="_blank">📱 03018573005</a>
      <a href="#enroll">💳 EasyPaisa: 03018573005</a>
      <a href="#enroll">🏦 Bank: 1644348071002307</a>
    </div>
  </div>
  <div class="footer-bottom">
    <div class="footer-copy">© 2025 WisdomWave Learning Institute — All rights reserved.</div>
    <div style="font-size:11px;color:var(--text3)">🔒 Secured</div>
  </div>
</footer>

<!-- POPUP -->
<div class="popup-overlay" id="popupOverlay">
  <div class="popup">
    <div class="popup-icon">✅</div>
    <h3>Enrollment Sent!</h3>
    <p>Your details have been sent to us on WhatsApp. Please complete these steps:</p>
    <div class="popup-steps">
      <div class="popup-step"><div class="ps-num">1</div><div>Send <strong>Rs. 2000</strong> to EasyPaisa <strong style="color:var(--gold)">03018573005</strong> or Bank <strong style="color:var(--gold)">1644348071002307</strong></div></div>
      <div class="popup-step"><div class="ps-num">2</div><div>Send payment screenshot to WhatsApp: <strong style="color:#25d366">03018573005</strong></div></div>
      <div class="popup-step"><div class="ps-num">3</div><div>You'll be added to the class group within 2 hours ✅</div></div>
    </div>
    <button class="popup-close" onclick="closePopup()">Got It! 👍</button>
  </div>
</div>

<script>
function toggleTheme(){
  const h=document.documentElement;
  const dark=h.getAttribute('data-theme')==='dark';
  h.setAttribute('data-theme',dark?'light':'dark');
  document.getElementById('themeBtn').textContent=dark?'☀️':'🌙';
}
function toggleMenu(){document.getElementById('mobileMenu').classList.toggle('open')}
function closeMenu(){document.getElementById('mobileMenu').classList.remove('open')}
function selectPay(el){
  document.querySelectorAll('.ppill').forEach(p=>p.classList.remove('active'));
  el.classList.add('active');
}
function enrollFor(course){
  document.getElementById('fcourse').value=course;
  document.getElementById('enroll').scrollIntoView({behavior:'smooth'});
  setTimeout(()=>document.getElementById('fname').focus(),600);
}
function submitEnroll(){
  const name=document.getElementById('fname').value.trim();
  const phone=document.getElementById('fphone').value.trim();
  const city=document.getElementById('fcity').value.trim();
  const course=document.getElementById('fcourse').value;
  const email=document.getElementById('femail').value.trim();
  const txn=document.getElementById('ftxn').value.trim();
  const notes=document.getElementById('fnotes').value.trim();
  const pay=document.querySelector('.ppill.active')?.textContent||'EasyPaisa';
  if(!name||!phone||!city||!course){
    alert('⚠️ Please fill in Name, WhatsApp Number, City and Course.');
    return;
  }
  let msg='🎓 *NEW ENROLLMENT — WISDOMWAVE LEARNING INSTITUTE*\n\n';
  msg+=`👤 *Name:* ${name}\n📱 *WhatsApp:* ${phone}\n🌍 *City:* ${city}\n`;
  if(email) msg+=`📧 *Email:* ${email}\n`;
  msg+=`📚 *Course:* ${course}\n💳 *Payment:* ${pay}\n`;
  if(txn) msg+=`🔢 *TXN ID:* ${txn}\n`;
  if(notes) msg+=`📝 *Message:* ${notes}\n`;
  msg+=`\n⏰ *Time:* ${new Date().toLocaleString()}\n✅ Please verify payment and add to WhatsApp group.`;
  document.getElementById('popupOverlay').classList.add('show');
  setTimeout(()=>window.open('https://wa.me/923018573005?text='+encodeURIComponent(msg),'_blank'),1200);
}
function closePopup(){document.getElementById('popupOverlay').classList.remove('show')}
document.getElementById('popupOverlay').addEventListener('click',function(e){if(e.target===this)closePopup()});
function updateCountdown(){
  const now=new Date(),target=new Date();
  target.setHours(17,0,0,0);
  if(now>=target) target.setDate(target.getDate()+1);
  const diff=target-now;
  const h=Math.floor(diff/3600000),m=Math.floor((diff%3600000)/60000),s=Math.floor((diff%60000)/1000);
  document.getElementById('t-hours').textContent=String(h).padStart(2,'0');
  document.getElementById('t-mins').textContent=String(m).padStart(2,'0');
  document.getElementById('t-secs').textContent=String(s).padStart(2,'0');
  const badge=document.getElementById('classBadge'),txt=document.getElementById('classTxt');
  const ch=now.getHours(),cm2=now.getMinutes();
  if(ch===17&&cm2<55){badge.className='class-badge';txt.textContent='🟢 Class is LIVE now!';}
  else if(h===0&&m<20){badge.className='class-badge';txt.textContent='⏳ Class starting very soon!';}
  else{badge.className='class-badge off';txt.textContent='Next class tomorrow at 5:00 PM';}
}
setInterval(updateCountdown,1000);
updateCountdown();
function toggleFaq(el){
  const item=el.parentElement,wasOpen=item.classList.contains('open');
  document.querySelectorAll('.faq-item').forEach(i=>i.classList.remove('open'));
  if(!wasOpen) item.classList.add('open');
}
const observer=new IntersectionObserver(entries=>{
  entries.forEach(e=>{if(e.isIntersecting) e.target.classList.add('visible');});
},{threshold:0.1});
document.querySelectorAll('.fade-in').forEach(el=>observer.observe(el));
</script>
</body>
</html>
