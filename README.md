<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Florida LE SOCE Focused Practice Exam — 100 Questions</title>
<style>
  :root{
    --navy:#0F2A3F;
    --navy-dark:#0A1D2D;
    --steel:#2E4A5E;
    --gold:#C8962E;
    --gold-light:#F4E3C1;
    --paper:#F7F5F0;
    --paper-line:#E4E0D5;
    --ink:#1C2730;
    --ink-soft:#54616B;
    --green:#2F6B3C;
    --green-bg:#E5F0E6;
    --red:#A3342E;
    --red-bg:#F8E6E4;
    --radius:6px;
  }
  *{box-sizing:border-box;margin:0;padding:0}
  html,body{background:var(--paper);color:var(--ink);font-family:'Georgia','Times New Roman',serif;line-height:1.6}
  body{padding-bottom:4rem}

  /* ===== HEADER / BADGE STRIP ===== */
  .masthead{
    background:linear-gradient(180deg,var(--navy) 0%, var(--navy-dark) 100%);
    color:#fff;
    padding:2rem 1.25rem 1.75rem;
    position:relative;
    overflow:hidden;
  }
  .masthead::before{
    content:"";
    position:absolute;
    top:0;left:0;right:0;bottom:0;
    background-image: repeating-linear-gradient(135deg, rgba(255,255,255,0.025) 0px, rgba(255,255,255,0.025) 2px, transparent 2px, transparent 14px);
    pointer-events:none;
  }
  .masthead-inner{max-width:760px;margin:0 auto;position:relative}
  .badge-row{display:flex;align-items:center;gap:14px;margin-bottom:0.85rem}
  .badge{
    width:52px;height:52px;border-radius:50%;
    border:2px solid var(--gold);
    display:flex;align-items:center;justify-content:center;
    font-family:Georgia,serif;font-weight:700;font-size:18px;letter-spacing:0.5px;
    color:var(--gold);
    background:rgba(200,150,46,0.08);
    flex-shrink:0;
  }
  .masthead-titles{flex:1}
  .eyebrow{
    font-family:'Helvetica Neue',Arial,sans-serif;
    text-transform:uppercase;
    letter-spacing:0.18em;
    font-size:11px;
    color:var(--gold-light);
    opacity:0.85;
    margin-bottom:4px;
  }
  .masthead h1{
    font-size:clamp(22px,5vw,32px);
    font-weight:700;
    letter-spacing:0.01em;
    line-height:1.15;
  }
  .masthead-sub{
    font-family:'Helvetica Neue',Arial,sans-serif;
    font-size:13px;
    color:rgba(255,255,255,0.75);
    margin-top:0.6rem;
    border-top:1px solid rgba(255,255,255,0.15);
    padding-top:0.6rem;
    display:flex;
    flex-wrap:wrap;
    gap:6px 18px;
  }
  .masthead-sub strong{color:var(--gold-light);font-weight:600}

  /* ===== CONTAINER ===== */
  .wrap{max-width:760px;margin:0 auto;padding:0 1.25rem}

  /* ===== SCOREBOARD ===== */
  .scoreboard{
    background:#fff;
    border:1px solid var(--paper-line);
    border-radius:var(--radius);
    margin-top:-1.5rem;
    position:relative;
    z-index:2;
    padding:1rem 1.25rem;
    box-shadow:0 6px 18px -10px rgba(15,42,63,0.35);
    font-family:'Helvetica Neue',Arial,sans-serif;
  }
  .progress-track{
    height:8px;background:var(--paper);border-radius:4px;overflow:hidden;border:1px solid var(--paper-line);
  }
  .progress-fill{
    height:100%;background:linear-gradient(90deg,var(--steel),var(--navy));
    width:0%;transition:width 0.35s ease;
  }
  .score-stats{
    display:flex;flex-wrap:wrap;gap:1.5rem;
    margin-top:0.75rem;
    font-size:12.5px;color:var(--ink-soft);
  }
  .score-stats b{color:var(--ink);font-size:14px;font-weight:700;display:block;font-family:Georgia,serif}
  .score-stat-label{text-transform:uppercase;letter-spacing:0.08em;font-size:10.5px;margin-bottom:2px;display:block}

  /* ===== FILTER BAR ===== */
  .filter-bar{
    font-family:'Helvetica Neue',Arial,sans-serif;
    display:flex;flex-wrap:wrap;gap:6px;
    margin:1.25rem 0 1.5rem;
  }
  .filter-chip{
    font-size:11.5px;
    padding:5px 12px;
    border-radius:20px;
    border:1px solid var(--paper-line);
    background:#fff;
    color:var(--ink-soft);
    cursor:pointer;
    transition:all 0.15s;
    white-space:nowrap;
  }
  .filter-chip:hover{border-color:var(--steel);color:var(--navy)}
  .filter-chip.active{
    background:var(--navy);
    border-color:var(--navy);
    color:#fff;
  }

  /* ===== ACTION ROW ===== */
  .action-row{
    display:flex;flex-wrap:wrap;gap:10px;margin-bottom:1.5rem;
    font-family:'Helvetica Neue',Arial,sans-serif;
  }
  .btn{
    font-family:'Helvetica Neue',Arial,sans-serif;
    font-size:13px;font-weight:600;
    padding:9px 18px;
    border-radius:var(--radius);
    border:1px solid var(--navy);
    background:#fff;
    color:var(--navy);
    cursor:pointer;
    transition:all 0.15s;
    letter-spacing:0.02em;
  }
  .btn:hover{background:var(--navy);color:#fff}
  .btn.primary{background:var(--navy);color:#fff}
  .btn.primary:hover{background:var(--navy-dark)}
  .btn:disabled{opacity:0.35;cursor:not-allowed}
  .btn:disabled:hover{background:#fff;color:var(--navy)}

  /* ===== QUESTION CARD ===== */
  .q-card{
    background:#fff;
    border:1px solid var(--paper-line);
    border-radius:var(--radius);
    padding:1.25rem 1.35rem;
    margin-bottom:1rem;
    position:relative;
  }
  .q-card::before{
    content:"";
    position:absolute;left:0;top:14px;bottom:14px;width:3px;
    background:var(--paper-line);
    border-radius:2px;
  }
  .q-card.answered.correct-pick::before{background:var(--green)}
  .q-card.answered.wrong-pick::before{background:var(--red)}

  .q-meta{
    font-family:'Helvetica Neue',Arial,sans-serif;
    display:flex;align-items:center;gap:10px;margin-bottom:0.6rem;flex-wrap:wrap;
  }
  .q-num{
    font-size:11px;font-weight:700;color:var(--navy);
    background:var(--gold-light);
    padding:2px 8px;border-radius:4px;
    letter-spacing:0.03em;
  }
  .q-topic{
    font-size:10.5px;text-transform:uppercase;letter-spacing:0.08em;
    color:var(--ink-soft);
  }
  .q-text{font-size:15.5px;color:var(--ink);margin-bottom:0.95rem;line-height:1.55}

  .choices{display:flex;flex-direction:column;gap:7px}
  .choice{
    display:flex;align-items:flex-start;gap:10px;
    padding:9px 12px;
    border:1px solid var(--paper-line);
    border-radius:var(--radius);
    cursor:pointer;
    font-size:14px;
    line-height:1.5;
    transition:background 0.12s,border-color 0.12s;
    background:var(--paper);
  }
  .choice:hover{border-color:var(--steel);background:#fff}
  .choice .letter{
    font-family:'Helvetica Neue',Arial,sans-serif;
    font-weight:700;font-size:12px;
    min-width:20px;height:20px;
    border-radius:50%;
    border:1px solid var(--paper-line);
    display:flex;align-items:center;justify-content:center;
    color:var(--ink-soft);
    flex-shrink:0;
    margin-top:1px;
    background:#fff;
  }
  .choice.selected{border-color:var(--navy);background:#fff}
  .choice.selected .letter{border-color:var(--navy);color:var(--navy);background:var(--gold-light)}
  .choice.correct{border-color:var(--green);background:var(--green-bg)}
  .choice.correct .letter{border-color:var(--green);color:#fff;background:var(--green)}
  .choice.wrong{border-color:var(--red);background:var(--red-bg)}
  .choice.wrong .letter{border-color:var(--red);color:#fff;background:var(--red)}
  .choice.disabled{cursor:default}
  .choice.disabled:hover{background:inherit}

  .explain{
    margin-top:0.85rem;padding-top:0.75rem;
    border-top:1px dashed var(--paper-line);
    font-family:'Helvetica Neue',Arial,sans-serif;
    font-size:12.5px;color:var(--ink-soft);
    line-height:1.6;
    display:none;
  }
  .explain.show{display:block}
  .explain b{color:var(--ink);font-weight:600}

  /* ===== RESULTS ===== */
  .results{
    background:#fff;border:1px solid var(--paper-line);border-radius:var(--radius);
    padding:2rem 1.5rem;text-align:center;margin-bottom:1.5rem;
  }
  .results-pct{font-size:56px;font-weight:700;color:var(--navy);font-family:Georgia,serif}
  .results-label{font-family:'Helvetica Neue',Arial,sans-serif;font-size:13px;color:var(--ink-soft);margin-top:2px;text-transform:uppercase;letter-spacing:0.1em}
  .results-verdict{
    margin-top:1.1rem;display:inline-block;
    font-family:'Helvetica Neue',Arial,sans-serif;
    font-weight:700;font-size:13px;letter-spacing:0.05em;
    padding:8px 20px;border-radius:20px;
  }
  .results-verdict.pass{background:var(--green-bg);color:var(--green)}
  .results-verdict.fail{background:var(--red-bg);color:var(--red)}
  .results-note{font-family:'Helvetica Neue',Arial,sans-serif;font-size:11.5px;color:var(--ink-soft);margin-top:0.6rem}

  .breakdown{
    display:grid;grid-template-columns:repeat(auto-fit,minmax(150px,1fr));
    gap:8px;margin-top:1.5rem;text-align:left;
    font-family:'Helvetica Neue',Arial,sans-serif;
  }
  .bd-item{background:var(--paper);border:1px solid var(--paper-line);border-radius:var(--radius);padding:10px 12px}
  .bd-topic{font-size:10px;text-transform:uppercase;letter-spacing:0.06em;color:var(--ink-soft);margin-bottom:3px}
  .bd-score{font-size:16px;font-weight:700;color:var(--navy);font-family:Georgia,serif}

  footer{
    max-width:760px;margin:2rem auto 0;padding:1rem 1.25rem;
    font-family:'Helvetica Neue',Arial,sans-serif;
    font-size:11px;color:var(--ink-soft);
    text-align:center;border-top:1px solid var(--paper-line);
  }

  @media (max-width:480px){
    .masthead{padding:1.5rem 1rem}
    .badge{width:44px;height:44px;font-size:15px}
    .scoreboard{margin-top:-1.25rem;padding:0.85rem 1rem}
    .q-card{padding:1rem}
  }

  /* ===== THEME TOGGLE BUTTON ===== */
  .theme-toggle{
    position:absolute;top:1rem;right:1rem;z-index:5;
    font-family:'Helvetica Neue',Arial,sans-serif;
    font-size:11.5px;font-weight:600;letter-spacing:0.04em;
    padding:6px 13px;border-radius:20px;
    border:1px solid var(--gold);
    background:rgba(200,150,46,0.12);
    color:var(--gold-light);
    cursor:pointer;transition:background 0.15s;
  }
  .theme-toggle:hover{background:rgba(200,150,46,0.24)}
  @media (max-width:480px){.theme-toggle{top:0.75rem;right:0.75rem;padding:5px 10px}}

  /* ===== DARK MODE ===== */
  [data-theme="dark"]{
    --paper:#0F1720;
    --paper-line:#2A3743;
    --ink:#E7ECF1;
    --ink-soft:#9DABB6;
    --steel:#3A5870;
    --green:#5BB36B;
    --green-bg:#16301D;
    --red:#E06A62;
    --red-bg:#391E1C;
    --card:#18222E;
  }
  /* Surfaces that hardcoded white in light mode */
  [data-theme="dark"] .scoreboard,
  [data-theme="dark"] .filter-chip,
  [data-theme="dark"] .q-card,
  [data-theme="dark"] .results,
  [data-theme="dark"] .choice .letter{background:var(--card)}
  [data-theme="dark"] .choice:hover{background:#1E2A38}
  [data-theme="dark"] .choice.selected{background:#1E2A38}
  [data-theme="dark"] .scoreboard{box-shadow:0 6px 18px -10px rgba(0,0,0,0.6)}
  /* Buttons: navy text is unreadable on dark surfaces, retint */
  [data-theme="dark"] .btn{background:var(--card);border-color:#3D5468;color:#CBD6E0}
  [data-theme="dark"] .btn:hover{background:#3D5468;color:#fff}
  [data-theme="dark"] .btn.primary{background:#24486A;border-color:#24486A;color:#fff}
  [data-theme="dark"] .btn.primary:hover{background:#2E5A84}
  [data-theme="dark"] .btn:disabled:hover{background:var(--card);color:#CBD6E0}
  [data-theme="dark"] .filter-chip:hover{border-color:var(--steel);color:var(--ink)}
  [data-theme="dark"] .filter-chip.active{background:#24486A;border-color:#24486A;color:#fff}
  /* Navy display text that needs to lighten on dark cards */
  [data-theme="dark"] .results-pct,
  [data-theme="dark"] .bd-score{color:var(--gold)}
</style>
</head>
<body>

<header class="masthead">
  <div class="masthead-inner">
    <button id="themeToggle" class="theme-toggle" onclick="toggleTheme()" aria-label="Toggle dark mode">Dark mode</button>
    <div class="badge-row">
      <div class="badge">FL</div>
      <div class="masthead-titles">
        <div class="eyebrow">Criminal Justice Standards &amp; Training Commission</div>
        <h1>SOCE Focused Practice Examination</h1>
      </div>
    </div>
    <div class="masthead-sub">
      <span><strong>Focus:</strong> Legal · Crimes Against Persons · Communication · Property · Serving Your Community</span>
      <span><strong>Questions:</strong> 100</span>
      <span><strong>Passing benchmark:</strong> 80 / 100 (80%)</span>
      <span><strong>Mix:</strong> 40% Legal</span>
    </div>
  </div>
</header>

<div class="wrap">
  <div class="scoreboard">
    <div class="progress-track"><div class="progress-fill" id="progressFill"></div></div>
    <div class="score-stats">
      <div>
        <span class="score-stat-label">Questions shown</span>
        <b id="statTotal">100</b>
      </div>
      <div>
        <span class="score-stat-label">Answered</span>
        <b id="statAnswered">0 / 100</b>
      </div>
      <div>
        <span class="score-stat-label">Running score</span>
        <b id="statScore">—</b>
      </div>
    </div>
  </div>

  <div class="filter-bar" id="filterBar"></div>

  <div class="action-row">
    <button class="btn primary" id="finishBtn" disabled onclick="showResults()">View final score</button>
    <button class="btn" onclick="resetAll()">Reset exam</button>
  </div>

  <div id="main"></div>
</div>

<footer>
  Built from the 2025 Florida Basic Recruit Training Program (Law Enforcement, Volume 1) and the FDLE SOCE Exam Content &amp; Preparation guide.<br>
  Focused review set covering the chapters your class flagged as deficient. Field-test questions are not represented here. This is an unofficial study aid.
</footer>

<script>
const ALL_QUESTIONS = [
{"id":1,"topic":"Legal","q":"Which standard of legal justification must an officer have before conducting a brief investigative stop of a person?","choices":["Probable cause","Proof beyond a reasonable doubt","Reasonable suspicion","Mere suspicion"],"answer":2,"explain":"An investigative stop requires reasonable suspicion — articulable facts supporting a suspicion that the person was committing, is committing, or is about to commit a law violation. Mere suspicion (a hunch) is not enough, and probable cause is the higher standard required for an arrest."},
{"id":2,"topic":"Legal","q":"Under the Fourth Amendment, a valid search warrant must, among other requirements, do which of the following?","choices":["Be approved by both the chief of police and the state attorney","Particularly describe the place to be searched and the persons or things to be seized","List the officer's training and experience with similar cases","Authorize a general search of the surrounding neighborhood"],"answer":1,"explain":"The Fourth Amendment requires that warrants be based on probable cause, supported by oath or affirmation, and particularly describe the place to be searched and the persons or things to be seized. The detailed description prevents intrusion into the wrong location."},
{"id":3,"topic":"Legal","q":"What is the primary purpose of the exclusionary rule?","choices":["To remove biased jurors from a criminal trial","To exclude officers who made procedural errors from the courtroom","To bar witnesses with criminal histories from testifying","To prevent evidence obtained through unconstitutional means from being used in court"],"answer":3,"explain":"The exclusionary rule prohibits the use of evidence obtained in violation of a person's constitutional rights, such as through an unlawful search or seizure. Failing to follow constitutional rules can result in suppression of evidence and confessions."},
{"id":4,"topic":"Legal","q":"Under the plain view doctrine, an officer may seize contraband without a warrant only when which set of conditions is met?","choices":["The officer obtains verbal consent after seeing the item","The officer is lawfully present, the item is in plain sight, and its criminal nature is immediately apparent","The officer has a search warrant for an adjacent location","The officer suspects the item may be evidence and photographs it first"],"answer":1,"explain":"Plain view requires three conditions: the officer is lawfully present where the item is seen, the item is in plain sight, and the officer has probable cause that the item is contraband or evidence — its criminal nature must be immediately apparent (see Sawyer v. State)."},
{"id":5,"topic":"Legal","q":"In Florida, a misdemeanor of the first degree is punishable by a maximum of:","choices":["1 year in jail and a $1,000 fine","60 days in jail and a $500 fine","30 days in jail and a $250 fine","5 years in prison and a $5,000 fine"],"answer":0,"explain":"A first-degree misdemeanor carries a maximum penalty of one year in a county jail, a fine of up to $1,000, or both. A second-degree misdemeanor is capped at 60 days and a $500 fine."},
{"id":6,"topic":"Legal","q":"Probable cause is best described as:","choices":["Absolute certainty that a particular person committed a crime","A fair probability or reasonable grounds, based on the totality of circumstances, to believe a crime was or is being committed","Any articulable suspicion that criminal activity may be occurring","An officer's hunch or gut feeling based on experience"],"answer":1,"explain":"Probable cause is the fair probability or reasonable grounds, based on the totality of circumstances, to believe a crime has been or is being committed. It is a stricter standard than reasonable suspicion but does not require certainty."},
{"id":7,"topic":"Legal","q":"Which constitutional amendment is best known for protecting against compelled self-incrimination?","choices":["Sixth Amendment","Fourth Amendment","Fifth Amendment","Eighth Amendment"],"answer":2,"explain":"The Fifth Amendment prohibits compelled self-incrimination. It also requires grand jury indictment for capital crimes and prohibits double jeopardy and deprivation of life, liberty, or property without due process."},
{"id":8,"topic":"Legal","q":"For a consent search to be valid, the consent must be:","choices":["Witnessed and signed by a supervisor","Given after the person is advised of the right to refuse","Knowing and voluntary, and given by a person with authority to consent","Obtained only after Miranda warnings are read"],"answer":2,"explain":"A consent search is valid when the consent is knowing and voluntary and the person has authority to consent. Officers are not required to advise people of the right to refuse. Voluntary means a reasonable person would feel free to refuse."},
{"id":9,"topic":"Legal","q":"Under the objective reasonableness standard established in Graham v. Connor, an officer's use of force is judged:","choices":["Solely by whether the suspect was ultimately found guilty","From the perspective of a reasonable officer on scene under the same tense, uncertain, and rapidly evolving circumstances","With the benefit of hindsight after all facts are known","By the least amount of force that could theoretically have been used"],"answer":1,"explain":"Graham v. Connor holds that use of force is examined under the Fourth Amendment's objective reasonableness standard, judged from the perspective of a reasonable officer on scene without the benefit of hindsight, considering the totality of the circumstances."},
{"id":10,"topic":"Legal","q":"Under Tennessee v. Garner and Florida law, deadly force may be used against a fleeing felon when:","choices":["The officer has exhausted every other available option","The suspect is fleeing a property crime scene","The suspect has committed any felony and refuses to stop","The officer has probable cause to believe the suspect poses a threat of death or serious bodily harm to the officer or others"],"answer":3,"explain":"Deadly force on a fleeing felon is justified only when there is probable cause that the suspect poses a threat of death or serious bodily harm to the officer or others. Where the suspect poses no such threat, deadly force to prevent escape is constitutionally unreasonable."},
{"id":11,"topic":"Legal","q":"Title 42 U.S.C. § 1983 allows civil lawsuits against:","choices":["Federal agencies that exceed their jurisdiction","Persons acting under color of state law who violate someone's constitutional rights","Corporations that refuse to cooperate with investigations","Private citizens who file false police reports"],"answer":1,"explain":"42 U.S.C. § 1983 is the most common federal statutory basis used to sue law enforcement officers. It provides a remedy when a person acting under color of state law intentionally violates a clearly established constitutional or civil right."},
{"id":12,"topic":"Legal","q":"Ordinances are laws that are:","choices":["Enacted by a municipal or county government and applied only within that jurisdiction","Issued by administrative agencies to govern their own operations","Created by appellate court decisions","Enacted by the U.S. Congress and applied nationwide"],"answer":0,"explain":"Ordinances are enacted by municipal (city) or county governments and apply only within that jurisdiction. They may be criminal or civil, but cannot conflict with state, federal, or case law."},
{"id":13,"topic":"Legal","q":"Once an appellate court establishes a rule of law, that rule is known as a precedent and an officer must:","choices":["Apply it only to cases in other circuits","Follow it only if their agency adopts it as policy","Follow it unless a higher court changes the rule","Disregard it if it conflicts with their training"],"answer":2,"explain":"Case law is formed by court decisions. Once an appellate court creates a precedent, officers are required to follow that rule unless a higher court changes it. Circuit court rulings are binding within that jurisdiction."},
{"id":14,"topic":"Legal","q":"In Florida, a third-degree felony carries a maximum penalty of:","choices":["15 years in a state correctional facility and a $10,000 fine","5 years in a state correctional facility and a $5,000 fine","1 year in county jail and a $1,000 fine","30 years in a state correctional facility and a $10,000 fine"],"answer":1,"explain":"A third-degree felony carries a maximum of 5 years in a state correctional facility, a $5,000 fine, or both. Aggravated assault is an example of a third-degree felony."},
{"id":15,"topic":"Legal","q":"Which class of offense is the highest classification of felony, carrying a penalty of death or life incarceration without the possibility of parole?","choices":["First-degree felony","Aggravated felony","Life felony","Capital felony"],"answer":3,"explain":"A capital felony is the highest class of felony. The penalty is death or life incarceration without the possibility of parole. First-degree murder is an example of a capital felony for which the state may impose the death penalty."},
{"id":16,"topic":"Legal","q":"A suspect aims a gun at one person, fires, misses, and unintentionally strikes a bystander. This scenario is an example of which category of criminal intent?","choices":["Specific intent","Transferred intent","General intent","Recklessness"],"answer":1,"explain":"Transferred intent occurs when a crime intended to harm one person inadvertently harms another instead, such as missing an intended target and striking a second victim. These situations are complex and warrant legal or supervisory advice."},
{"id":17,"topic":"Legal","q":"Which of the following is an example of a specific intent crime?","choices":["Assault","Battery","Involuntary manslaughter","Burglary"],"answer":3,"explain":"Specific intent crimes are usually done intentionally, knowingly, purposely, or willfully. Examples include burglary, embezzlement, forgery, murder, robbery, and theft. Battery, assault, and involuntary manslaughter are general intent crimes."},
{"id":18,"topic":"Legal","q":"The four elements that must all be proven to establish negligence are:","choices":["Motive, opportunity, means, and intent","Probable cause, reasonable suspicion, force, and injury","A duty to act with care, breach of that duty, causation (proximate cause), and damages","Knowledge, willfulness, malice, and harm"],"answer":2,"explain":"The four elements of negligence are a duty to act with care, breach of that duty, causation or proximate cause, and damages. If any one element is missing, the defendant cannot be found negligent."},
{"id":19,"topic":"Legal","q":"The three main types of law enforcement encounters are:","choices":["Interviews, interrogations, and depositions","Detentions, frisks, and seizures","Consensual encounters, investigative stops, and arrests","Traffic stops, pat downs, and searches"],"answer":2,"explain":"The three main types of encounters are consensual encounters (no/mere suspicion), investigative stops (reasonable suspicion), and arrests (probable cause). Each must have a corresponding level of suspicion."},
{"id":20,"topic":"Legal","q":"Which of the following would most likely convert a consensual encounter into an investigative stop?","choices":["Making polite conversation with a local business owner","Listening to information the person voluntarily provides","Asking a community member how their day is going","Activating the patrol vehicle's emergency lights to stop the person"],"answer":3,"explain":"A consensual encounter is voluntary, and the person must feel free to leave. Using sirens or red/blue lights, blocking the person's path, giving commands, or physically restraining the person raises the encounter to an investigative stop or seizure."},
{"id":21,"topic":"Legal","q":"The two elements required for a lawful Terry pat down (frisk) are that the person is lawfully detained based on reasonable suspicion, and:","choices":["The person has refused to identify themselves","The person is in a high-crime area","The officer has a warrant for the person's arrest","The officer has reasonable suspicion to believe the person possesses a dangerous weapon"],"answer":3,"explain":"A lawful frisk requires that the person be lawfully detained on reasonable suspicion AND that the officer have reasonable suspicion the person is armed with a dangerous weapon. An officer may not automatically pat down everyone detained."},
{"id":22,"topic":"Legal","q":"Under the plain touch/feel doctrine, an officer conducting a lawful frisk may seize an item that:","choices":["Is immediately and readily recognized as contraband by touch","Feels like it could possibly be evidence after manipulation","Resembles a weapon in shape only","Is located in a locked container"],"answer":0,"explain":"The plain touch/feel doctrine (Minnesota v. Dickerson) allows seizure of an item immediately recognized as contraband by touch during a valid frisk. It does not permit manipulation or groping of the object to identify it."},
{"id":23,"topic":"Legal","q":"Based on Whren v. United States, a traffic stop based on an observed traffic infraction is valid even if the officer's real motive is to investigate other criminal activity. Such a stop is known as a:","choices":["Terry stop","Consensual stop","High-risk stop","Pretext stop"],"answer":3,"explain":"A pretext stop occurs when an officer stops a vehicle for an observed traffic or equipment violation but is actually interested in other criminal activity. Per Whren, the officer's subjective motive is irrelevant if there is an objectively reasonable basis for the stop."},
{"id":24,"topic":"Legal","q":"The standard of proof required to find a criminal defendant guilty at trial is:","choices":["Proof beyond a reasonable doubt","Preponderance of the evidence","Probable cause","Clear and convincing evidence"],"answer":0,"explain":"Proof beyond a reasonable doubt is the standard used to determine guilt. The prosecution must prove each element of the crime to this standard. Probable cause supporting an arrest is not, by itself, enough to prove guilt at trial."},
{"id":25,"topic":"Legal","q":"Under the Carroll doctrine (mobile conveyance exception), a vehicle may be searched without a warrant because:","choices":["Vehicles have no expectation of privacy at all","A driver automatically consents to a search by driving on public roads","Officers may always search any container they choose","Vehicles are licensed, registered, and easily moved, giving them a reduced expectation of privacy — but probable cause is still required"],"answer":3,"explain":"Under the Carroll doctrine, vehicles have a reduced expectation of privacy because they are regulated and mobile. A warrantless search is allowed, but probable cause is still required, and the scope extends to all parts of the vehicle where the evidence could reasonably be found."},
{"id":26,"topic":"Legal","q":"Fresh pursuit, as an exigent circumstance, allows an officer to:","choices":["Search any home in the neighborhood for a suspect","Use deadly force regardless of the threat the suspect poses","Stop pursuit and obtain a warrant before continuing","Arrest a fleeing suspect even after the suspect crosses jurisdictional lines"],"answer":3,"explain":"Fresh pursuit is the immediate and continuous pursuit of a fleeing suspect. It permits an officer to make an arrest even when the suspect crosses jurisdictional lines, provided the offense occurred within the pursuing officer's jurisdiction and the pursuit is continuous."},
{"id":27,"topic":"Legal","q":"A vehicle inventory search is permitted without a warrant because its purpose is to:","choices":["Search for evidence of additional crimes","Establish probable cause for the original arrest","Locate contraband that probable cause would not otherwise permit","Document and protect the arrested person's property and protect the agency from theft or damage claims"],"answer":3,"explain":"An inventory documents valuable property in a vehicle to protect the arrested person's property and shield the officer and agency from accusations of theft, loss, or damage. It is permitted only when the vehicle is impounded, and any contraband found may still be used in court."},
{"id":28,"topic":"Legal","q":"Under Arizona v. Gant, officers may search the passenger compartment of a vehicle incident to a recent occupant's arrest only when:","choices":["A canine has alerted on the exterior of the vehicle","The arrest was for a felony offense","The arrestee is unsecured and within reaching distance of the compartment, or it is reasonable to believe the vehicle contains evidence of the crime of arrest","The vehicle is registered to someone other than the arrestee"],"answer":2,"explain":"Arizona v. Gant refined search incident to arrest for vehicles: officers may search the passenger compartment only when the arrestee is unsecured and within reaching distance, or when it is reasonable to believe the vehicle contains evidence of the crime for which the person was arrested."},
{"id":29,"topic":"Legal","q":"Searching the contents of a trash can placed at the curb for pickup is generally permissible without a warrant because:","choices":["Trash is always considered contraband","The owner has abandoned any reasonable expectation of privacy in the trash","Curbside trash is government property","A warrant exception specifically lists trash cans"],"answer":1,"explain":"Abandoned property, such as trash placed at the curb for pickup, is not protected because the owner has abandoned any reasonable expectation of privacy in it. Without a reasonable expectation of privacy, the action is not a Fourth Amendment search."},
{"id":30,"topic":"Legal","q":"Under Florida's concealed carry law effective July 1, 2023 (HB 543), an individual may carry a concealed firearm without a license if they meet certain conditions, including being:","choices":["Registered with the local sheriff's office","A resident of Florida for at least five years","A current or former member of the military","21 years of age or older and not otherwise prohibited from possessing a firearm"],"answer":3,"explain":"Following HB 543, Florida allows carrying a concealed weapon or firearm without a license if conditions are met, generally including being 21 or older and not otherwise prohibited from possessing a firearm. The firearm must be concealed from ordinary sight."},
{"id":31,"topic":"Legal","q":"A risk protection order (RPO) is a court order that:","choices":["Temporarily restricts a person's access to firearms for up to one year when they pose a significant danger to themselves or others","Requires a person to surrender their driver's license","Permanently revokes a person's right to ever own a firearm","Authorizes an arrest for a domestic violence offense"],"answer":0,"explain":"An RPO temporarily restricts a person's access to firearms and ammunition for up to one year when they pose a significant danger to themselves or others. The petition must include a sworn affidavit and identify the firearms and ammunition the person controls."},
{"id":32,"topic":"Legal","q":"An officer may make a warrantless arrest for a misdemeanor that did NOT occur in their presence in which of the following situations?","choices":["A noise complaint from a neighbor","A parking violation","An act of domestic violence","Public intoxication reported by a witness"],"answer":2,"explain":"Florida law lists statutory exceptions to the in-presence requirement for misdemeanor arrests, including acts of domestic violence, battery, retail theft, stalking, and criminal mischief, among others. These allow a probable-cause arrest even when the officer did not witness the act."},
{"id":33,"topic":"Legal","q":"An officer may NOT issue a notice to appear in lieu of physical arrest when:","choices":["The accused has a local address","The offense is a county ordinance violation","The accused's identity cannot be verified or the accused refuses to sign","The offense is a first-degree misdemeanor"],"answer":2,"explain":"A notice to appear cannot be issued when, among other things, the accused's identity cannot be verified, the accused refuses to sign, domestic violence may be involved, or the accused poses an unreasonable risk of harm. It is available only for certain misdemeanors and ordinance/criminal traffic violations."},
{"id":34,"topic":"Legal","q":"Florida's sovereign immunity law (s. 768.28, F.S.) generally protects individual officers from personal liability in state tort actions unless the officer:","choices":["Used any level of force","Acted with willful or wanton disregard of someone's rights or property","Made an arrest without a warrant","Failed to issue a citation"],"answer":1,"explain":"Sovereign immunity is a limited waiver that protects individual officers from personal liability in state tort actions unless they act with willful or wanton disregard of someone's rights or property. It covers only state tort actions, not federal civil rights claims."},
{"id":35,"topic":"Legal","q":"When an agency is held responsible for the negligent actions of its officer due to negligence in training, hiring, supervision, or retention, this is known as:","choices":["Sovereign immunity","Direct liability","Criminal liability","Vicarious liability"],"answer":3,"explain":"Vicarious liability is the indirect responsibility an agency bears for an officer's actions due to negligence in training, hiring, assignment, supervision, direction, or retention. Direct liability arises from the agency's own action or failure to act regarding a policy violation."},
{"id":36,"topic":"Legal","q":"Under Florida law, the first appearance hearing must occur within how long after an arrest?","choices":["12 hours","72 hours","48 hours","24 hours"],"answer":3,"explain":"Florida law requires the first appearance hearing to occur within 24 hours of arrest. At first appearance, the judge appoints counsel if the defendant qualifies and reviews the probable cause affidavit to decide if probable cause exists."},
{"id":37,"topic":"Legal","q":"In Florida's state court system, which court has jurisdiction over felony cases, divorce, and civil cases involving amounts over $50,000?","choices":["District court of appeal","Florida Supreme Court","Circuit court","County court"],"answer":2,"explain":"The 20 circuit courts handle major criminal offenses (felonies), domestic relations cases, probate, civil cases over $50,000, and Baker Act and Marchman Act cases. County courts handle misdemeanors, ordinance violations, and civil cases of $50,000 or less."},
{"id":38,"topic":"Legal","q":"A person who acts under color of law and intentionally deprives another of a constitutional or civil right may be prosecuted under which federal statute?","choices":["The Posse Comitatus Act","Title VII","18 U.S.C. § 242","42 U.S.C. § 1983"],"answer":2,"explain":"18 U.S.C. § 242 is the federal criminal statute that prohibits anyone acting under color of law from willfully depriving a person of constitutional or civil rights. (42 U.S.C. § 1983 is the parallel civil statute.)"},
{"id":39,"topic":"Legal","q":"A person who aids, abets, counsels, hires, or persuades another to commit a crime, and may be charged whether or not present when the crime occurred, is classified as:","choices":["A principal in the first degree","An accessory after the fact","An accomplice in the second degree","A material witness"],"answer":0,"explain":"A principal in the first degree is a person who commits, or who aids, abets, counsels, hires, or persuades another to commit an offense. A principal may be charged whether or not present when the crime was committed. An accessory after the fact helps a principal avoid detection or punishment."},
{"id":40,"topic":"Legal","q":"A pretrial proceeding in which witnesses and involved parties (except the defendant) give separate sworn testimony to an attorney before trial is called a:","choices":["Arraignment","Sentencing hearing","Deposition","Suppression hearing"],"answer":2,"explain":"A deposition is a pretrial proceeding in which involved parties, except the defendant, give separate sworn testimony to one of the attorneys. It allows the attorneys to assess the case and document testimony before trial. An officer should review the transcript before testifying."},
{"id":41,"topic":"Crimes Against Persons","q":"Marsy's Law in Florida primarily requires officers to:","choices":["Photograph every crime scene before interviewing victims","Obtain a confession before filing charges","Provide victims and their families with information about their rights","Arrest a suspect within 24 hours of any reported crime"],"answer":2,"explain":"Marsy's Law requires officers to provide all victims and their families with information about their rights, including due process, freedom from intimidation, timely notice of proceedings, and protection from the accused. Officers document providing victims' rights brochures in their reports."},
{"id":42,"topic":"Crimes Against Persons","q":"Which of the following describes the crime of assault under Florida law?","choices":["Confining a person against their will","An intentional, unlawful threat by word or act that creates a well-founded fear of imminent violence in the victim","Intentionally touching or striking another person against their will","Causing great bodily harm with a deadly weapon"],"answer":1,"explain":"Assault is an intentional, unlawful threat — by word or act — to do violence, where the suspect appears able to carry it out and creates a well-founded fear that violence is imminent. Battery, by contrast, requires an actual touching or striking."},
{"id":43,"topic":"Crimes Against Persons","q":"A battery charge is reclassified to aggravated battery when the suspect:","choices":["Intentionally or knowingly causes great bodily harm, permanent disability, or disfigurement, or uses a deadly weapon","Threatens the victim with words","Acts in the presence of a law enforcement officer","Touches the victim only once"],"answer":0,"explain":"Aggravated battery requires that the suspect committed battery and either intentionally/knowingly caused great bodily harm, permanent disability, or permanent disfigurement, or used a deadly weapon. Battery against a person known to be pregnant is also aggravated battery."},
{"id":44,"topic":"Crimes Against Persons","q":"In a Florida domestic violence incident where probable cause exists, arrest is the preferred response for:","choices":["The party who called law enforcement","Both parties involved in the dispute","The primary aggressor, not a person acting reasonably in self-defense","Whichever party the victim identifies"],"answer":2,"explain":"When probable cause exists that domestic violence occurred between family or household members, arrest is the preferred response only for the primary aggressor — not for a person who acted reasonably to protect themselves or a family member from violence."},
{"id":45,"topic":"Crimes Against Persons","q":"Under Florida law, the charge filed after an arrest at a domestic violence incident will be:","choices":["The underlying offense such as battery or aggravated assault, with the relationship determining that it is domestic","A charge of 'domestic violence' itself","Determined solely by the victim's preference","Always a felony regardless of the conduct"],"answer":0,"explain":"In Florida, there is no charge titled 'domestic violence.' The actual charge is the underlying offense (e.g., assault, battery, aggravated assault). The relationship between the perpetrator and victim determines whether the incident is classified as domestic violence."},
{"id":46,"topic":"Crimes Against Persons","q":"Stalking under Florida law requires that the suspect:","choices":["Has a prior relationship with the victim","Makes a single threatening phone call","Willfully, maliciously, and repeatedly follows, harasses, or cyberstalks the victim","Follows the victim one time to learn their address"],"answer":2,"explain":"Stalking occurs when a suspect willfully, maliciously, and repeatedly follows, harasses, or cyberstalks a victim. A single incident generally does not qualify. Aggravated stalking adds a credible threat that places the victim in reasonable fear."},
{"id":47,"topic":"Crimes Against Persons","q":"Suspected child abuse, neglect, or abandonment must be reported by calling:","choices":["The DCF Abuse Hotline","The state attorney's office within 72 hours","The local school principal","The child's other parent"],"answer":0,"explain":"Florida law requires everyone to report any suspicion or knowledge of child abuse, neglect, or abandonment by calling the DCF (Department of Children and Families) Abuse Hotline. Professionals such as law enforcement must provide their names when reporting."},
{"id":48,"topic":"Crimes Against Persons","q":"Under Florida's Baby Safe Haven provisions, a parent does NOT commit abuse, neglect, or abandonment if they surrender an infant who is approximately:","choices":["30 days old or younger at a hospital, EMS station, or fire station","1 year old or younger at a daycare facility","6 months old or younger at a police station","7 days old or younger at any private home"],"answer":0,"explain":"A parent may surrender an infant approximately 30 days old or younger at a hospital, emergency room, EMS station, or fire station without committing abuse, neglect, or abandonment. Unless abuse is suspected, the parent may remain anonymous and may not be pursued."},
{"id":49,"topic":"Crimes Against Persons","q":"The key difference between false imprisonment and kidnapping is that kidnapping includes:","choices":["The use of a deadly weapon","A victim who is a minor","Moving the victim a greater distance","The intent to commit another felony, such as ransom, a felony, or terrorizing the victim"],"answer":3,"explain":"Both involve forcible confinement against the victim's will, but kidnapping requires the additional intent to hold for ransom, commit or assist a felony, inflict harm or terrorize, or interfere with a government function. False imprisonment requires no such additional intent."},
{"id":50,"topic":"Crimes Against Persons","q":"Which alert is used specifically for a missing adult who suffers from dementia, Alzheimer's disease, or other qualifying cognitive impairment?","choices":["AMBER Alert","Blue Alert","Purple Alert","Silver Alert"],"answer":3,"explain":"A Silver Alert aids in the recovery of a missing adult who suffers from dementia, Alzheimer's, or other qualifying cognitive impairment. The subject must generally be 60 or older, or 18–59 lacking capacity with verified irreversible cognitive deterioration."},
{"id":51,"topic":"Crimes Against Persons","q":"An AMBER Alert requires several criteria, including a clear indication of abduction, a detailed description, and that the child is:","choices":["Last seen with a stranger","Younger than 12 years of age","Younger than 18 years of age and whose life is determined to be in danger","Missing for at least 24 hours"],"answer":2,"explain":"An AMBER Alert requires that the child be younger than 18, that there is a clear indication of abduction, that the agency of jurisdiction recommends activation, that a detailed description is available, and that the investigation concludes the child's life is in danger."},
{"id":52,"topic":"Crimes Against Persons","q":"Under Florida law, which category of person is incapable of giving consent to sexual activity because they are unconscious, asleep, or otherwise physically unable to communicate unwillingness?","choices":["Mentally defective","Physically helpless","Physically incapacitated","Mentally incapacitated"],"answer":1,"explain":"A 'physically helpless' person is unconscious, asleep, or for any other reason physically unable to communicate unwillingness to an act. This is one of the statutory categories of persons incapable of giving consent in a sexual battery case."},
{"id":53,"topic":"Crimes Against Persons","q":"Human trafficking is distinguished from many other crimes by its core element of:","choices":["Transportation across an international border","Exploitation of a person through force, fraud, or coercion for labor or commercial sex","The use of a weapon","A juvenile victim in every case"],"answer":1,"explain":"Human trafficking involves exploitation through force, fraud, or coercion for the purpose of forced labor or commercial sex. (For victims under 18, force, fraud, or coercion need not be proven for sex trafficking.) Transportation across a border is not required."},
{"id":54,"topic":"Crimes Against Persons","q":"When investigating an undetermined death, the officer's manner of death determination — natural, accident, suicide, homicide, or undetermined — is ultimately made by:","choices":["The responding officer alone","The medical examiner, in conjunction with law enforcement's investigation","The victim's family physician","The state attorney's office"],"answer":1,"explain":"The five manners of death are natural, accident, suicide, homicide, and undetermined. The officer and medical examiner cannot determine cause and manner independently; the ME, working with law enforcement's investigation, makes the final determination. Officers treat undetermined deaths as potential homicides."},
{"id":55,"topic":"Crimes Against Persons","q":"Robbery differs from theft because robbery requires:","choices":["The use of force, violence, assault, or putting the victim in fear during the taking","A higher dollar value of property","Premeditation and planning","Property taken from a business rather than a person"],"answer":0,"explain":"Robbery is a crime against a person: it requires the taking of property with intent to deprive AND the use of force, violence, assault, or placing the victim in fear during the taking. Theft and burglary are property crimes lacking this direct person-to-person element."},
{"id":56,"topic":"Communication","q":"Empathy, as a communication tool for officers, is best described as:","choices":["Agreeing with everything a person says","Telling a person how they should feel","Feeling sad for someone in a difficult situation","The ability to understand and care about the emotions of others"],"answer":3,"explain":"Empathy is the ability to understand and care about the emotions of others — putting yourself in another person's shoes. It should not be confused with sympathy, which is feeling sad for someone. Empathy helps officers connect with people and keep situations safe."},
{"id":57,"topic":"Communication","q":"An officer's most valuable non-verbal tool, demonstrated through confidence, professional appearance, erect posture, and alertness, is known as:","choices":["Command presence","Procedural justice","Active listening","Self-disclosure"],"answer":0,"explain":"Command presence is an officer's most valuable non-verbal tool. It is demonstrated through confidence, a professional appearance, erect posture, alertness, and attention to surroundings. Training, education, and experience improve command presence."},
{"id":58,"topic":"Communication","q":"The LEED framework, used to remain professional in interactions, stands for:","choices":["Locate, Evaluate, Enforce, Document","Lead, Engage, Educate, Defend","Listen, Explain, Equity, Dignity","Listen, Empathize, Encourage, Decide"],"answer":2,"explain":"The LEED framework — Listen, Explain, Equity, Dignity — provides guidelines that help officers remain professional in a variety of situations and supports the four pillars of procedural justice."},
{"id":59,"topic":"Communication","q":"Which of the following best describes active listening in a law enforcement context?","choices":["Giving full attention, then paraphrasing, summarizing, clarifying, and reflecting to confirm understanding","Writing detailed notes while the person speaks so nothing is missed","Allowing dispatch to record the conversation so the officer can focus elsewhere","Interrupting frequently to keep the conversation on track"],"answer":0,"explain":"Active listening involves giving full attention and using techniques such as paraphrasing, summarizing, clarifying, and reflecting — while allowing adequate time for the person to respond. It focuses more on listening than talking to gather accurate information."},
{"id":60,"topic":"Communication","q":"When using a sign language or spoken-language interpreter, the officer should:","choices":["Avoid eye contact to prevent intimidation","Speak directly to the interpreter and let them relay the message","Rely on a family member rather than a qualified interpreter in confrontational situations","Speak directly to the person and maintain eye contact with them, not the interpreter"],"answer":3,"explain":"When an interpreter is present, the officer should speak directly to the person and maintain eye contact with them, not the interpreter. In potentially confrontational situations, officers should not rely on family, friends, or children to interpret, as the information may be biased."},
{"id":61,"topic":"Communication","q":"To maintain the consensual nature of an encounter, an officer should:","choices":["Take possession of the person's identification","Position a vehicle to block the person's path","Allow the person to leave and end the conversation at any time","Activate emergency lights to gain attention"],"answer":2,"explain":"To keep an encounter consensual, the officer must allow the person to leave or end the conversation at any time, avoid blocking their path, not force them to identify themselves, not frisk or restrain them, and not use commands or emergency lights."},
{"id":62,"topic":"Communication","q":"Which of the following is one of the 10 core communication competencies officers should demonstrate?","choices":["Speaking only in writing to create a record","Using technical jargon to convey authority","Active listening","Avoiding all emotional expression"],"answer":2,"explain":"The 10 core communication competencies include introduction, appropriate questions, active listening, self-de-escalation, non-verbal communication, environment/audience consideration, implicit bias awareness, self-awareness, procedural justice, and appropriate conclusion."},
{"id":63,"topic":"Communication","q":"When receiving profanity or name-calling from a member of the public, an officer should remember that:","choices":["The officer should respond with equal force of language","The person is generally attacking the profession, not the officer personally, so the officer should focus on behavior rather than language","The encounter should end immediately","The behavior justifies an immediate arrest for disorderly conduct"],"answer":1,"explain":"When on the receiving end of profanity or name-calling, officers should remember the person is attacking the profession, not them personally. Focus on the person's behavior rather than their language; if they comply with a lawful request, that behavior matters more than what they say."},
{"id":64,"topic":"Communication","q":"In communication, a 'break of gaze' occurs when a person drops their gaze from the person looking at them and may indicate:","choices":["Any number of emotions or non-verbal messages, and should not lead to quick assumptions","That the person is committing a crime","That the person is not listening","Definite guilt or deception"],"answer":0,"explain":"A break of gaze may be caused by personality, emotional state, a traumatic event, cultural norms, or recalling information. It may indicate any number of emotions — officers should not be quick to assume they understand the response when a person breaks eye contact."},
{"id":65,"topic":"Communication","q":"Which of the following is an effective conflict-resolution strategy when mediating a dispute?","choices":["Take immediate enforcement action against both parties","Separate the people involved in a safe location where they cannot communicate with one another","Refuse to explain any of the officer's actions","Keep the parties together so they can confront each other"],"answer":1,"explain":"Effective conflict resolution includes separating the people involved in a safe location where they cannot communicate, rendering first aid if needed, gathering information from all sides, providing options and resources, and acting to leave people with their dignity intact."},
{"id":66,"topic":"Communication","q":"Which technique helps an officer mentally prepare for an interaction by recalling training and visualizing a professional response?","choices":["Reflective listening","Mutual gaze","Self-talk","Command presence"],"answer":2,"explain":"Self-talk is the practice of talking to yourself as you anticipate or evaluate an event — recalling training, applying agency policy, and visualizing a professional response. It helps officers remain objective and keep their emotional responses in check."},
{"id":67,"topic":"Communication","q":"When giving directions to a person during a stressful or noisy situation, the officer should:","choices":["Use slang to build rapport","Use long, detailed explanations to be thorough","Rely on hand gestures alone","Give clear, specific directions and keep sentences brief and to the point"],"answer":3,"explain":"To overcome communication barriers, officers should keep sentences brief, give clear and specific directions (e.g., 'stand next to the trunk of your car' rather than 'move over there'), use open-ended questions, and allow the person to give their side."},
{"id":68,"topic":"Communication","q":"Being culturally responsive as an officer means:","choices":["Being open to learning about new cultures, respecting differences, and recognizing the role culture plays in people's lives","Treating everyone exactly the same regardless of background","Assuming all members of a culture behave identically","Avoiding interaction with people from unfamiliar cultures"],"answer":0,"explain":"Cultural responsiveness means being open to learning about new cultures, respecting cultural differences, and recognizing the important role culture plays in people's lives. Officers improve intercultural communication by learning about their community and admitting and fixing mistakes."},
{"id":69,"topic":"Communication","q":"Self-de-escalation, one of the core communication competencies, refers to an officer's ability to:","choices":["End a conversation by issuing commands","Pause and reset their own response when becoming angry or emotional, including withdrawing or being relieved by another officer","Use physical force to control a situation","De-escalate an angry member of the public"],"answer":1,"explain":"Self-de-escalation is the officer's ability to manage their own emotions — pausing to reset, withdrawing from a conversation, or having a fellow officer take over. Self-control helps officers stay emotionally strong under stress and avoid escalating a situation."},
{"id":70,"topic":"Communication","q":"Non-verbal communication includes which of the following?","choices":["Written incident reports","Body language, facial expressions, eye contact, and personal space","The wording of an official press release","Radio transmissions between officers"],"answer":1,"explain":"Non-verbal communication is any message sent without the explicit use of language. It includes voice and tone, appearance, posture, body movement, facial expressions, touch, smell, personal space, and eye contact."},
{"id":71,"topic":"Crimes Involving Property","q":"Under Florida law, grand theft generally involves the theft of property valued at:","choices":["$750 or more","$100 or more","$500 or more","$300 or more"],"answer":0,"explain":"Grand theft involves property valued at $750 or more, certain items specified by statute regardless of value, or items worth $40 or more taken from a dwelling. Theft of $100 up to $750 is first-degree petit theft; under $100 is second-degree petit theft."},
{"id":72,"topic":"Crimes Involving Property","q":"Burglary, as defined under Florida law, requires that a person:","choices":["Enter or remain in a dwelling, structure, or conveyance with the intent to commit an offense inside, without being licensed or invited","Take property directly from another person by force","Damage another person's property willfully","Break and enter a structure using a tool"],"answer":0,"explain":"Burglary is the unlawful entry into (or remaining in) a structure or conveyance with the intent to commit a crime inside, when not licensed, invited, or otherwise authorized. Forcible 'breaking' is not required — entering with criminal intent is sufficient."},
{"id":73,"topic":"Crimes Involving Property","q":"Criminal mischief is committed when a person:","choices":["Possesses tools that could be used for vandalism","Enters property without permission","Willfully and maliciously injures or damages the real or personal property of another","Threatens to damage property to extort money"],"answer":2,"explain":"Criminal mischief is the willful and malicious destruction of or damage to another person's real or personal property, including graffiti and vandalism. Penalties increase with the value of the damage, and prior convictions can elevate it to a felony."},
{"id":74,"topic":"Crimes Involving Property","q":"Which crime can result in a warrantless arrest even when the offense was NOT committed in the officer's presence?","choices":["Loitering and prowling","Trespassing on private property","Disorderly intoxication","Retail theft"],"answer":3,"explain":"Florida law allows a warrantless arrest for retail theft even when the offense is not committed in the officer's presence, provided there is probable cause. Retail theft is one of the statutory exceptions to the in-presence requirement for misdemeanor arrests."},
{"id":75,"topic":"Crimes Involving Property","q":"The key distinction between trespassing and burglary is that burglary additionally requires:","choices":["The intent to commit another crime inside the structure","The presence of the property owner","Damage to the property","A posted no-trespassing sign"],"answer":0,"explain":"Both trespassing and burglary involve being somewhere without authorization. Burglary adds the element of intent to commit another crime, such as theft, inside the structure. Robbery, by contrast, involves taking property from a person by force or fear."},
{"id":76,"topic":"Crimes Involving Property","q":"In white-collar crime, the difference between forgery and uttering is that uttering involves:","choices":["Stealing a blank check","Creating or altering a false document","Possessing counterfeit currency","Knowingly publishing or attempting to pass a forged document as genuine"],"answer":3,"explain":"Forgery is altering, forging, or counterfeiting a document with intent to defraud. Uttering is knowingly exhibiting, publishing, or attempting to pass a forged document — such as cashing a check — while claiming it is genuine."},
{"id":77,"topic":"Crimes Involving Property","q":"The act of using a device attached to a point-of-sale terminal to capture a customer's credit card information during a transaction is called:","choices":["Phishing","Carding","Uttering","Skimming"],"answer":3,"explain":"Skimming is extracting a customer's credit card information using a skimming device attached to a point-of-sale device, which stores the data as payment is processed. Phishing, by contrast, uses fake digital communication to obtain information from victims."},
{"id":78,"topic":"Crimes Involving Property","q":"Which of the following best describes identity theft?","choices":["Using another person's name in conversation without permission","Failing to return borrowed property","Possessing a fake ID for novelty purposes","The unlawful possession or use of a person's identifying information to commit fraud, such as opening accounts or obtaining credit"],"answer":3,"explain":"Identity theft is the unlawful possession or use of a person's identifying information to commit acts of fraud — applying for credit or loans, acquiring services, taking over accounts, or committing crimes. A detective typically investigates these cases."},
{"id":79,"topic":"Crimes Involving Property","q":"In Florida, aggravated animal cruelty — which involves a cruel death or excessive or repeated infliction of unnecessary pain or suffering — is classified as a:","choices":["Second-degree misdemeanor","Civil infraction","Felony","First-degree misdemeanor"],"answer":2,"explain":"Aggravated animal cruelty, which involves intentionally causing a cruel death or excessive or repeated infliction of unnecessary pain or suffering, is a felony in Florida. Basic cruelty to animals (e.g., depriving an animal of necessary food or shelter) is a misdemeanor."},
{"id":80,"topic":"Crimes Involving Property","q":"Loitering or prowling becomes a chargeable offense when a person lingers in a place, at a time, or in a manner not usual for law-abiding people, AND:","choices":["The person is in a public park","The person is simply out at an odd hour","Under circumstances that raise alarm or immediate concern for the safety of persons or property nearby","The person refuses to make eye contact"],"answer":2,"explain":"Loitering or prowling requires lingering without apparent purpose in a manner unusual for law-abiding people, under circumstances that raise alarm or immediate concern for safety of persons or property. Being out at an odd hour alone does not justify the charge; officers should initiate a consensual encounter to dispel concerns."},
{"id":81,"topic":"Crimes Involving Property","q":"A person who simply curses at an officer or others may generally NOT be arrested for disorderly conduct unless:","choices":["The person refuses to apologize","Other factors are present that threaten the safety of the officer or others, or the words incite a dangerous reaction","The words are spoken loudly","More than one officer is present"],"answer":1,"explain":"Freedom of speech protects a person who merely curses. Disorderly conduct requires that the person's actions endanger the safety of others or property, or that the words actually incite a dangerous reaction (e.g., shouting 'fire' in a crowded theater)."},
{"id":82,"topic":"Crimes Involving Property","q":"The crime of allowing an open house party requires that the person who is 18 or older and controls the residence:","choices":["Charged admission to the party","Knowingly allowed a minor to possess or consume alcohol or drugs at the residence during the party","Failed to obtain a permit for the gathering","Allowed loud music after 10 p.m."],"answer":1,"explain":"An open house party violation requires that a person 18 or older who controls the residence allowed the party and knowingly allowed a minor to possess or consume alcohol or drugs there. A social gathering itself is legal unless minors consume alcohol or drugs."},
{"id":83,"topic":"Crimes Involving Property","q":"The Florida Comprehensive Drug Abuse Prevention and Control Act (chapter 893, F.S.) places controlled substances into how many schedules, based on medicinal value, harmfulness, and potential for misuse?","choices":["Three","Five","Four","Seven"],"answer":1,"explain":"Chapter 893, F.S., the Florida Comprehensive Drug Abuse Prevention and Control Act, places all controlled substances into one of five schedules based on medicinal value, harmfulness, and the potential for misuse and addiction."},
{"id":84,"topic":"Crimes Involving Property","q":"In robbery by sudden snatching, which element is NOT required (unlike standard robbery)?","choices":["That the suspect intended to deprive the victim of the property","That the property was taken from the victim's person","That the victim became aware of the taking","The use of force, violence, or threats beyond the snatching itself"],"answer":3,"explain":"Robbery by sudden snatching requires that property be taken from the victim's person and that the victim became aware of the taking, but it does NOT require the use of force, violence, or threats beyond the snatching. Standard robbery requires force, violence, assault, or fear."},
{"id":85,"topic":"Crimes Involving Property","q":"For trespassing to apply, a 'person authorized' to order someone to depart the property includes:","choices":["Any member of the public who feels threatened","Only a uniformed law enforcement officer","An owner, lessee, their agent, or an officer whose agency received written authorization from the owner","A neighbor who witnesses the trespass"],"answer":2,"explain":"A 'person authorized' in trespassing means an owner or lessee, their agent, or a law enforcement officer whose agency received written authorization from the owner or lessee to communicate an order to depart in cases of threats to public safety or welfare."},
{"topic":"Serving Your Community","q":"Under Florida law, a vulnerable adult is defined as a person 18 or older whose ability to perform the activities of daily living or provide for their own care or protection is impaired due to:","choices":["A mental, emotional, sensory, long-term physical or developmental disability, brain damage, or the infirmities of aging","Low income or homelessness alone","A criminal record","A language barrier"],"answer":0,"explain":"A vulnerable adult is a person 18 or older whose ability to perform daily living activities or provide for their own care or protection is impaired due to a mental, emotional, sensory, long-term physical or developmental disability, brain damage, or the infirmities of aging.","id":86},
{"topic":"Serving Your Community","q":"According to chapter 825, F.S., an elderly person is defined as a person who is:","choices":["70 years of age or older living alone","60 years of age or older suffering from the infirmities of aging that impair their ability to care for or protect themselves","65 years of age or older","55 years of age or older"],"answer":1,"explain":"Chapter 825, F.S., defines an elderly person as someone 60 years of age or older suffering from the infirmities of aging — manifested by advanced age, organic brain damage, or other dysfunction — to the extent their ability to provide for their own care or protection is impaired.","id":87},
{"topic":"Serving Your Community","q":"Which of the following best distinguishes dementia from Alzheimer's disease?","choices":["Alzheimer's only affects people under 60","Dementia is an umbrella term for organic, progressive mental disorders, while Alzheimer's is a specific progressive brain disorder","Dementia is always reversible with treatment","They are identical conditions with different names"],"answer":1,"explain":"Dementia is an umbrella term describing an organic, progressive mental disorder marked by memory loss and impaired judgment. Alzheimer's disease is a specific progressive brain disorder that gradually destroys memory and the ability to learn, reason, and carry out daily activities.","id":88},
{"topic":"Serving Your Community","q":"Under Florida law, a juvenile is defined as a person younger than 18, though research notes the brain is not fully developed until approximately age:","choices":["25","21","30","16"],"answer":0,"explain":"Florida law defines a juvenile as a person younger than 18. However, the brain is not fully developed until about age 25, which may help explain the risky behavior or lack of impulse control juveniles and young adults can exhibit.","id":89},
{"topic":"Serving Your Community","q":"When an officer encounters a runaway child, they should:","choices":["Take no action since running away is not a crime","Issue the child a citation and release them","Take the child into protective custody and contact the parent or legal guardian","Arrest the child for being a runaway"],"answer":2,"explain":"Officers have no arrest authority for a child who is a runaway, but should always presume the child is in danger. If you believe a child is a runaway, take them into protective custody and contact the parent or guardian (or DCF if unavailable). Protective custody is not a criminal arrest.","id":90},
{"topic":"Serving Your Community","q":"When responding to an incident involving a veteran who may have a traumatic brain injury (TBI) or PTSD, one of the biggest mistakes an officer can make is to:","choices":["Try to gain the person's trust","Speak in a calm voice","Request backup from an officer with a military background","Corner the person unnecessarily"],"answer":3,"explain":"Cornering a veteran who might have TBI or PTSD is one of the biggest mistakes an officer can make, because combat training may lead them to battle. Officers should gain trust, avoid cornering unless necessary, and consider backup from an officer with a military background. TBI symptoms can also mimic intoxication.","id":91},
{"topic":"Serving Your Community","q":"Under Florida law, a homeless person is defined as someone who:","choices":["Does not have a fixed, regular, and adequate nighttime residence","Has committed a vagrancy offense","Lives in a vehicle by choice","Refuses offers of shelter"],"answer":0,"explain":"Florida law defines homeless as a person who does not have a fixed, regular, and adequate nighttime residence. Being homeless is not a crime; officers can provide information about services instead of making an arrest and should treat the person with dignity and respect.","id":92},
{"topic":"Serving Your Community","q":"Under the ADA, a person with a disability is someone who has a physical or mental impairment that:","choices":["Is documented by a physician","Substantially limits a major life activity, has a record of such impairment, or is regarded as having one","Requires the use of a wheelchair","Prevents them from working entirely"],"answer":1,"explain":"Under the ADA, a person with a disability has a physical or mental impairment that substantially limits a major life activity, has a record of such impairment, or is regarded as having one. Major life activities include caring for oneself, walking, seeing, hearing, learning, and working.","id":93},
{"topic":"Serving Your Community","q":"Autism spectrum disorder (ASD) can be difficult to recognize because:","choices":["It is always accompanied by a physical disability","It does not always have visual indicators, and the person may display self-stimulating behaviors such as body rocking or hand flapping","It always has clear visual indicators","It only affects communication, never behavior"],"answer":1,"explain":"ASD can be difficult to recognize because it does not always have visual indicators. A person on the spectrum may display self-stimulating behaviors such as body rocking, hand flapping, skin picking, or finger flicking. Recognizing and approaching the person appropriately can make a significant difference in the outcome.","id":94},
{"topic":"Serving Your Community","q":"How does mental illness differ from a developmental disability?","choices":["They are the same condition","Mental illness refers to disturbances in how people process thoughts, emotions, and behaviors and can occur at any time, while developmental disabilities involve intellectual functioning and occur before adulthood","Mental illness deals with below-average intellectual functioning while developmental disabilities involve thought and emotional processes","Mental illness only occurs in people with low intelligence"],"answer":1,"explain":"Mental illness refers to disturbances in how people process thoughts, emotions, and behaviors and can occur at any time in life. Developmental disabilities involve below-average intellectual functioning and the ability to learn, and occur before a person reaches adulthood. Mental illness is not related to intelligence.","id":95},
{"id":96,"topic":"Serving Your Community","q":"Under the Baker Act, a person may be taken into custody for an involuntary examination when there is reason to believe they have a mental illness AND:","choices":["They are simply being difficult to deal with","They refuse to answer the officer's questions","They have a prior psychiatric history","They are likely to cause serious bodily harm to themselves or others, or are unable to care for themselves"],"answer":3,"explain":"The Baker Act authorizes involuntary examination when a person has a mental illness and is likely to cause serious bodily harm to themselves or others, or is unable to care for themselves. Officers should not use the Baker Act simply to deal with difficult people."},
{"id":97,"topic":"Serving Your Community","q":"The Marchman Act provides for involuntary assessment and stabilization of a person who, because of substance abuse impairment:","choices":["Has a co-occurring physical disability","Refuses to leave a public place","Has lost the power of self-control and is in need of substance abuse services","Has committed a drug-related felony"],"answer":2,"explain":"The Marchman Act addresses involuntary assessment and stabilization for substance abuse. It applies when there is good-faith reason to believe a person is substance-abuse impaired, has lost the power of self-control, and is in need of services or poses a danger."},
{"id":98,"topic":"Serving Your Community","q":"Under Florida law, a criminal gang is defined as a formal or informal ongoing group whose primary activities include criminal acts and that consists of:","choices":["A formal organization with elected officers and bylaws","Three or more persons who have a common name or common identifying signs, colors, or symbols","Two or more persons related by blood","Any group of juveniles who gather in public"],"answer":1,"explain":"A criminal gang is a formal or informal ongoing group whose primary activities include criminal or delinquent acts and that consists of three or more persons with a common name or common identifying signs, colors, or symbols — including terrorist organizations and hate groups."},
{"id":99,"topic":"Serving Your Community","q":"Under the ADA, when it is not obvious whether an animal is a service animal, an officer may ask only which two questions?","choices":["The owner's diagnosis and treating physician","Whether the dog is required because of a disability, and what work or task it has been trained to perform","For the animal's certification papers and vaccination records","The animal's breed and its age"],"answer":1,"explain":"Under the ADA, when it is not obvious that an animal is a service animal, an officer may ask only two questions: is the dog a service animal required because of a disability, and what work or task has it been trained to perform. No certification is required under the law."},
{"id":100,"topic":"Serving Your Community","q":"Extremist groups are primarily distinguished from typical criminal gangs by the fact that extremist groups:","choices":["Operate only at the federal level","Always have a formal organizational structure","Are motivated by an ideology and seek to advance it through force or violence","Never engage in any criminal activity"],"answer":2,"explain":"Extremist groups advocate violence and illegal disruption of others' lawful activities to advance an ideology. While antigovernment or offensive speech alone is protected by the First Amendment, seeking to advance that ideology through force or violence is illegal — the ideological motivation distinguishes them from profit-driven criminal gangs."}
];

const TOPICS = [...new Set(ALL_QUESTIONS.map(q=>q.topic))];

let answers = {};
let currentFilter = 'All';
let showingResults = false;

function getFiltered(){
  if(currentFilter==='All') return ALL_QUESTIONS;
  return ALL_QUESTIONS.filter(q=>q.topic===currentFilter);
}

function buildFilterBar(){
  const bar = document.getElementById('filterBar');
  let html = `<button class="filter-chip active" data-filter="All" onclick="setFilter('All')">All topics</button>`;
  TOPICS.forEach(t=>{
    html += `<button class="filter-chip" data-filter="${t}" onclick="setFilter('${t}')">${t}</button>`;
  });
  bar.innerHTML = html;
}

function setFilter(f){
  currentFilter = f;
  document.querySelectorAll('.filter-chip').forEach(c=>{
    c.classList.toggle('active', c.getAttribute('data-filter')===f);
  });
  render();
}

function updateScoreboard(){
  const total = ALL_QUESTIONS.length;
  const answeredAll = Object.keys(answers).length;
  const correctAll = ALL_QUESTIONS.filter(q=>answers[q.id]===q.answer).length;

  document.getElementById('progressFill').style.width = Math.round(answeredAll/total*100) + '%';
  document.getElementById('statTotal').textContent = total;
  document.getElementById('statAnswered').textContent = answeredAll + ' / ' + total;
  document.getElementById('statScore').textContent = answeredAll>0
    ? correctAll + ' / ' + answeredAll + ' (' + Math.round(correctAll/answeredAll*100) + '%)'
    : '—';

  document.getElementById('finishBtn').disabled = answeredAll < total;
}

function render(){
  updateScoreboard();
  const el = document.getElementById('main');

  if(showingResults){
    renderResults(el);
    return;
  }

  const qs = getFiltered();
  let html = '';

  qs.forEach(q=>{
    const sel = answers[q.id];
    const submitted = sel !== undefined;
    let cardClass = 'q-card';
    if(submitted){
      cardClass += ' answered';
      cardClass += (sel === q.answer) ? ' correct-pick' : ' wrong-pick';
    }

    html += `<div class="${cardClass}">`;
    html += `<div class="q-meta"><span class="q-num">Q${q.id}</span><span class="q-topic">${q.topic}</span></div>`;
    html += `<div class="q-text">${q.q}</div>`;
    html += `<div class="choices">`;

    q.choices.forEach((c,i)=>{
      let cls = 'choice';
      if(submitted){
        cls += ' disabled';
        if(i === q.answer) cls += ' correct';
        else if(i === sel) cls += ' wrong';
      } else if(sel === i){
        cls += ' selected';
      }
      const letter = 'ABCD'[i];
      html += `<div class="${cls}" onclick="answer(${q.id},${i})"><span class="letter">${letter}</span><span>${c}</span></div>`;
    });

    html += `</div>`;

    if(submitted){
      html += `<div class="explain show"><b>Explanation:</b> ${q.explain}</div>`;
    }

    html += `</div>`;
  });

  const scrollY = window.scrollY;
  el.innerHTML = html;
  window.scrollTo(0, scrollY);
}

function renderResults(el){
  const total = ALL_QUESTIONS.length;
  const correct = ALL_QUESTIONS.filter(q=>answers[q.id]===q.answer).length;
  const pct = Math.round(correct/total*100);
  const pass = correct >= 80;

  let html = `<div class="results">`;
  html += `<div class="results-pct">${pct}%</div>`;
  html += `<div class="results-label">${correct} of ${total} correct</div>`;
  html += `<div class="results-verdict ${pass?'pass':'fail'}">${pass ? 'PASS — meets the 80% benchmark' : 'BELOW PASSING — under 80%'}</div>`;
  html += `<div class="results-note">SOCE pass standard: 80% correct. This focused set uses 80 of 100 as the benchmark.</div>`;

  html += `<div class="breakdown">`;
  TOPICS.forEach(t=>{
    const qs = ALL_QUESTIONS.filter(q=>q.topic===t);
    const c = qs.filter(q=>answers[q.id]===q.answer).length;
    html += `<div class="bd-item"><div class="bd-topic">${t}</div><div class="bd-score">${c} / ${qs.length}</div></div>`;
  });
  html += `</div>`;

  html += `<div class="action-row" style="justify-content:center;margin-top:1.5rem">`;
  html += `<button class="btn primary" onclick="reviewAnswers()">Review answers</button>`;
  html += `<button class="btn" onclick="resetAll()">Retake exam</button>`;
  html += `</div>`;
  html += `</div>`;

  el.innerHTML = html;
  window.scrollTo({top:0});
}

function reviewAnswers(){
  showingResults = false;
  currentFilter = 'All';
  setFilter('All');
}

function resetAll(){
  answers = {};
  showingResults = false;
  currentFilter = 'All';
  setFilter('All');
}

function answer(id, choice){
  if(answers[id] !== undefined) return;
  answers[id] = choice;
  render();
}

function showResults(){
  showingResults = true;
  render();
}

function applyTheme(t){
  if(t==='dark') document.documentElement.setAttribute('data-theme','dark');
  else document.documentElement.removeAttribute('data-theme');
  const btn = document.getElementById('themeToggle');
  if(btn) btn.textContent = (t==='dark') ? 'Light mode' : 'Dark mode';
}

function toggleTheme(){
  const isDark = document.documentElement.getAttribute('data-theme')==='dark';
  const next = isDark ? 'light' : 'dark';
  try{ localStorage.setItem('soce-theme', next); }catch(e){}
  applyTheme(next);
}

(function initTheme(){
  let t = 'light';
  try{ t = localStorage.getItem('soce-theme') || 'light'; }catch(e){}
  applyTheme(t);
})();

buildFilterBar();
render();
</script>
</body>
</html>
