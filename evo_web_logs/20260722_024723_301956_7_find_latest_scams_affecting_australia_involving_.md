# EVO Web Run

- Run ID: `20260722_024723_301956_7`
- Started: `2026-07-22T02:47:23`
- Query: Find latest scams affecting Australia involving AI

## Metadata

- 55592d91-b45c-49db-a967-731627428571
- Run id: 2YwOilgzyiFuA-TbvklVd7FNgVZfWVWY
- Conversation id: 55592d91-b45c-49db-a967-731627428571
- Trace log: evo_web_logs/20260722_024723_301956_7_find_latest_scams_affecting_australia_involving_.md

## Tool Trace

- Tier 0 triage: REASON
- Requesting capabilities: web_lookup, Class
- [OK] Prolog full trace
--- prolog source ---

:- dynamic active_assumption/1.

problem_spec(spec(
    'AI Scams Affecting Australia',
    'Identify latest scams involving artificial intelligence affecting Australians, including methods, platforms, and notable examples.',
    [requirement(identify_scams, 'List specific AI-enabled scam types targeting Australians'),
     requirement(describe_methods, 'Describe how AI is used in each scam type'),
     requirement(cite_sources, 'Provide recent authoritative sources'),
     requirement(temporal, 'Focus on latest/recent scams as of mid-2026')]
)).

spec_requirement(identify_scams, 'List specific AI-enabled scam types targeting Australians').
spec_requirement(describe_methods, 'Describe how AI is used in each scam type').
spec_requirement(cite_sources, 'Provide recent authoritative sources').
spec_requirement(temporal, 'Focus on latest/recent scams as of mid-2026').

need_capability(web_lookup, 'Current news and government sources on AI scams affecting Australia in 2025-2026').

main :-
    writeln(problem_spec(spec(_, _, _))),
    forall(need_capability(Class, Purpose),
           writeln(need_capability(Class, Purpose))).

:- main.
--- prolog output ---
problem_spec(spec(_6148,_6150,_6152))
need_capability(web_lookup,Current news and government sources on AI scams affecting Australia in 2025-2026)
- Web search: latest AI scams Australia 2025 2026 artificial intelligence
- [OK] Web Search Results with Extracted Content
================================================================================

Source: Brave
Query: "latest AI scams Australia 2025 2026 artificial intelligence fraud"
Results: 5

================================================================================

## Result 1: 26-063MR ASIC ramps-up action to protect consumers from AI-powered online investment scams | ASIC
URL: https://www.asic.gov.au/about-asic/news-centre/find-a-media-release/2026-rele
- Web search: Australian government AI scam warning 2026 Scamwatch
- [OK] Web Search Results with Extracted Content
================================================================================

Source: Brave
Query: "Australian government AI scam warning 2026 Scamwatch"
Results: 5

================================================================================

## Result 1: AI Powered Bank Scams Australia 2026: How Aussies Are Being Targeted
URL: https://scamdekho.in/global/ai-powered-bank-scams-australia-2026

**Extracted Content:**
Home
Services
PayPal Email Che
- Web search: deepfake AI voice cloning scam Australia 2025 2026
- [OK] Web Search Results with Extracted Content
================================================================================

Source: Brave
Query: "deepfake AI voice cloning scam Australia 2025 2026"
Results: 5

================================================================================

## Result 1: AI voice cloning scams cost Australians AUD $25.8m
URL: https://securitybrief.com.au/story/ai-voice-cloning-scams-cost-australians-aud-25-8m

**Extracted Content:**
SecurityBrief Australia - Tech
- Browsing www.abc.net.au
- [OK] Web Page: https://www.abc.net.au/news/2026-04-07/asic-warning-ai-supercharging-scams/106538526

Title: AI supercharging online scams as regulator ASIC takes down almost 12,000 sites in a year - ABC News

Content:
SKIP TO MAIN CONTENT
SKIP TO NEWS NAVIGATION, SETTINGS AND SEARCH
Explore the ABC
More from ABC
NEWS
IVIEW
LISTEN
Log In
Log In
ABC News
Just In
For You
Politics
World
Business
More
Search the ABC
Start typing for suggestions, press enter to search, or choose from a list of options belo
- Web search: AI chatbot romance scam Australia 2026 pig butchering
- [OK] Web Search Results with Extracted Content
================================================================================

Source: Brave
Query: "AI chatbot romance scam Australia 2026 pig butchering"
Results: 5

================================================================================

## Result 1: AI supercharges industrial-scale online romance scams
URL: https://itbrief.com.au/story/ai-supercharges-industrial-scale-online-romance-scams

**Extracted Content:**
IT Brief Australia - Techn
- Browsing scamdekho.in
- [OK] Web Page: https://scamdekho.in/global/ai-powered-bank-scams-australia-2026

Title: AI Powered Bank Scams Australia 2026: How Aussies Are Being Targeted

Content:
Home
Services 
 PayPal Email Checker  PayPal Invoice Checker  Message Scam Checker  Website / URL Checker  Screenshot Scam Checker  UPI & QR Code Checker
 Job Offer Letter Checker
Report Scam
Blog
Global
About
Home› Global› AI Powered Bank Scams Australia 2026: How Aussies Are Being Targeted
 Global Scam Alert
AI Powered Bank Scams Aust
- Web search: deepfake celebrity endorsement scam Australia 2026 investmen
- [OK] Web Search Results with Extracted Content
================================================================================

Source: Brave
Query: "deepfake celebrity endorsement scam Australia 2026 investment crypto AI generated"
Results: 5

================================================================================

## Result 1: How AI Deepfakes Are Fueling Crypto Scams in 2026
URL: https://bluntmag.com.au/gaming/ai-deepfake-crypto-scams-2026

**Extracted Content:**
Skip to content
Main Nav
- Web search: AI job scam Australia 2026 fake recruitment "money mule"
- [OK] Web Search Results with Extracted Content
================================================================================

Source: Brave
Query: "AI job scam Australia 2026 fake recruitment "money mule""
Results: 5

================================================================================

## Result 1: Westpac warns of AI driven scam surge | Westpac
URL: https://www.westpac.com.au/about-westpac/media/media-releases/2026/2-april/

**Extracted Content:**
Skip to main content
Skip to main na
- Web search: "pig butchering" AI Australia 2025 2026 romance investment s
- [OK] Web Search Results with Extracted Content
================================================================================

Source: LangSearch
Query: ""pig butchering" AI Australia 2025 2026 romance investment scam"
Results: 5

================================================================================

## Result 1: Bynarivonexa.com Scam Review: Quantum AI Trading Allegations and the Fake Investment Platform Warning - ForteClaim
URL: https://forteclaim.com/bynarivonexa-com-scam-review-quant
- Browsing www.asic.gov.au
- [OK] Web Page: https://www.asic.gov.au/about-asic/news-centre/find-a-media-release/2026-releases/26-063mr-asic-ramps-up-action-to-protect-consumers-from-ai-powered-online-investment-scams/

Title: 26-063MR ASIC ramps-up action to protect consumers from AI-powered online investment scams | ASIC

Content:
Media releases
Reports and Publications
ASIC's views
Bannings and Alerts

Newsroom

Print Share
MEDIA RELEASE (26-063MR)
ASIC ramps-up action to protect consumers from AI-powered online investment sca
- Browsing securitybrief.com.au
- [OK] Web Page: https://securitybrief.com.au/story/ai-voice-cloning-scams-cost-australians-aud-25-8m

Title: AI voice cloning scams cost Australians AUD $25.8m

Content:
SecurityBrief Australia - Technology news for CISOs & cybersecurity decision-makers
AUSTRALIA
POWERED BY
GUIDES
Cloud Security
Cybersecurity
Endpoint Protection
Firewalls
Ransomware
PHISHING
PHYSICAL SECURITY
EMAIL SECURITY
AI voice cloning scams cost Australians AUD $25.8m
Wed, 4th Feb 2026
MARK TARRE
News Chief

Swinburne University
- Web search: Westpac AI scam warning 2026 Ben Young deepfake fraud Austra
- [OK] Web Search Results with Extracted Content
================================================================================

Source: LangSearch
Query: "Westpac AI scam warning 2026 Ben Young deepfake fraud Australia"
Results: 5

================================================================================

## Result 1: AI Powered Bank Scams Australia 2026: How Aussies Are Being Targeted
URL: https://scamdekho.in/global/ai-powered-bank-scams-australia-2026

**Search Snippet:**
global scam alert
- Formalizing knowledge base: scam_types_identified, ai_is_scaling_factor, voice_cloning_is_key_threat
- [OK] Prolog full trace
--- prolog source ---

%% --- Harness ---
:- dynamic active_assumption/1.

prove(Goal, proved(Goal)) :- call(Goal).

contradictory_pair(_X, _Y) :- false.
are_contradictory(_X, _Y) :- false.
inconsistent :- contradictory_pair(_, _).

solved(Name, Status) :-
    conclusion(Conclusion),
    prove(conclusion(Conclusion), _Proof),
    fulfills(Conclusion, Name, Status).

fulfills(Conclusion, Name, fulfilled) :-
    conclusion(Conclusion),
    spec_requirement(Name, _).

%% --- Problem spec ---
problem_spec(spec(
    'AI Scams Affecting Australia (2025-2026)',
    'Identify and describe the latest AI-enabled scam types affecting Australians.',
    [requirement(identify_scams, 'List specific AI-enabled scam types targeting Australians'),
     requirement(describe_methods, 'Describe how AI is used in each scam type'),
     requirement(cite_sources, 'Provide recent authoritative sources'),
     requirement(temporal, 'Focus on latest/recent scams as of mid-2026')]
)).

spec_requirement(identify_scams, 'List specific AI-enabled scam types targeting Australians').
spec_requirement(describe_methods, 'Describe how AI is used in each scam type').
spec_requirement(cite_sources, 'Provide recent authoritative sources').
spec_requirement(temporal, 'Focus on latest/recent scams as of mid-2026').

%% --- Acquired facts (R3: INGEST) ---

% Source: ASIC Media Release 26-063MR, 8 April 2026
acquired_fact(asic('26-063MR', '2026-04-08'),
    'ASIC removed 11,964 scam websites in 2025 (90% increase from 2024). AI supercharging scams.').
acquired_fact(asic('26-063MR', '2026-04-08'),
    'ASIC took down over 1,100 investment scam ads on social media in 2025.').
acquired_fact(asic('26-063MR', '2026-04-08'),
    'Australians lost $2.18 billion to scams in 2025; investment scams accounted for $837.7 million.').
acquired_fact(asic('26-063MR', '2026-04-08'),
    'AI used for polished fake investment ads, fake endorsements, cloaking to hide content.').
acquired_fact(asic('26-063MR', '2026-04-08'),
    'AI trading bots falsely claimed to generate passive income and unrealistic returns.').

% Source: ABC News, 7 April 2026
acquired_fact(abc_news('2026-04-07'),
    'Professor Paul Haskell-Dowland (ECU): AI has turned cybercrime into a supermarket aisle; scammers spin up 100 websites at a flick of a switch.').
acquired_fact(abc_news('2026-04-07'),
    'ASIC Commissioner Alan Kirkland: AI used to create new websites rapidly and as a gloss to attract investment.').
acquired_fact(abc_news('2026-04-07'),
    'Job scams surging, particularly targeting young people.').

% Source: Swinburne University / SecurityBrief Australia, 4 Feb 2026
acquired_fact(swinburne('2026-02-04'),
    'AI voice cloning scams cost Australians $25.8 million in first half of 2025.').
acquired_fact(swinburne('2026-02-04'),
    'Voice cloning can replicate family members voices from social media samples for Hi Mum scams and ransom-style attacks.').
acquired_fact(swinburne('2026-02-04'),
    'AI expert Dominique Carlon: voice cloning is most confronting new scam tool; urgency is key warning signal.').

% Source: Scamdekho.in, 11 May 2026 (synthesizing multiple sources)
acquired_fact(scamdekho('2026-05-11'),
    'Deepfake celebrity investment ads: AI clones faces and voices of well-known Australians for fake investment videos on Facebook, Instagram, YouTube.').
acquired_fact(scamdekho('2026-05-11'),
    'AI-powered phishing emails use correct names, bank names, and reference recent transactions, mimicking official bank communications perfectly.').
acquired_fact(scamdekho('2026-05-11'),
    'Commonwealth Bank identified suspected $1 billion loan fraud racket using AI-generated fake financial documents for home loans.').
acquired_fact(scamdekho('2026-05-11'),
    'Westpac Head of Fraud Ben Young warned of highly targeted, intensely personal AI attacks beyond generic phishing.').

% Source: Illawarra Mercury / ACCC National Anti-Scam Centre, June 2026
acquired_fact(accc_nasc('2026-06-24'),
    'ACCC National Anti-Scam Centre: 200,600 scams reported in 2025 with losses exceeding $330 million.').
acquired_fact(accc_nasc('2026-06-24'),
    'Scammers use AI, deepfake identities, and cloned websites resembling legitimate organisations.').

%% --- Scam types identified ---
scam_type(1, 'AI Deepfake Celebrity Investment Ads',
    'AI clones faces/voices of Australian celebrities (business figures, TV personalities) for fake investment videos on social media. Videos urge quick sign-up; deposited money vanishes.').
scam_type(2, 'AI Voice Cloning (Hi Mum / Family Emergency)',
    'AI clones a family members voice from seconds of social media audio. Victim receives urgent call from cloned voice claiming to be in trouble, needing immediate money transfer.').
scam_type(3, 'AI-Powered Phishing Emails & SMS',
    'AI generates perfectly written, personalized messages referencing victims real name, bank, and recent transactions. Mimics official bank communications to steal login credentials.').
scam_type(4, 'AI-Generated Fake Investment Platforms & Trading Bots',
    'AI creates polished websites and ads claiming AI-powered trading bots generate guaranteed high returns. 11,964 such sites removed by ASIC in 2025 alone.').
scam_type(5, 'AI-Facilitated Loan & Property Fraud',
    'AI generates fake financial documents (payslips, tax returns, bank statements) for fraudulent loan applications. CBA flagged suspected $1 billion racket in early 2026.').
scam_type(6, 'AI-Powered Romance / Pig Butchering Scams',
    'AI chatbots build trust over weeks/months through romantic relationships, then direct victims to fake investment platforms (pig butchering). Large-scale, industrialized operations.').
scam_type(7, 'AI-Generated Job Scams & Money Mule Recruitment',
    'AI creates convincing job ads and recruitment communications. Targets young people to share bank details or act as money mules for laundering scam proceeds.').
scam_type(8, 'AI Cloaking & Platform Evasion',
    'AI hides scam content from platform moderators by displaying different content based on device, location, or viewer profile. Enables scammers to evade takedown.').

%% --- Rules ---
conclusion(scam_types_identified) :-
    findall(_, scam_type(_, _, _), L),
    length(L, N),
    N >= 5.

conclusion(ai_is_scaling_factor) :-
    acquired_fact(abc_news('2026-04-07'), _),
    acquired_fact(asic('26-063MR', '2026-04-08'), _).

conclusion(voice_cloning_is_key_threat) :-
    acquired_fact(swinburne('2026-02-04'), _).

conclusion(regulatory_response_active) :-
    acquired_fact(asic('26-063MR', '2026-04-08'), _).

conclusion(multi_billion_dollar_scale) :-
    acquired_fact(asic('26-063MR', '2026-04-08'), _).

conclusion(ai_lowers_barrier_to_entry) :-
    acquired_fact(abc_news('2026-04-07'), _).

conclusion(institutional_fraud_enabled) :-
    acquired_fact(scamdekho('2026-05-11'), _).

%% --- Assumptions ---
assumption(sources_authoritative,
    'Web sources (ASIC, ABC News, Swinburne University, ACCC) are authoritative and factually accurate for 2025-2026.').
assumption(scam_classification_complete,
    'The eight identified scam types represent the major AI-enabled scam categories but may not be exhaustive.').

activate :-
    forall(assumption(A, _),
           ( \+ active_assumption(A) ->
               assertz(active_assumption(A))
           ; true
           )).

main :-
    activate,
    prove(problem_spec(_), _),
    write('R3: evidence ingested from 5+ authoritative sources'), nl,
    findall(Answer-Proof,
            (conclusion(Answer), prove(conclusion(Answer), Proof)),
            Results),
    length(Results, Count),
    write('R4: derived '), write(Count), write(' conclusion(s)'), nl,
    (Results = [] -> true ;
     forall(member(Answer-Proof, Results),
            (write('  Conclusion: '), write(Answer), nl,
             write('    Proof: '), write(Proof), nl))),
    (inconsistent ->
        write('R5: KB IS INCONSISTENT'), nl
    ;
        write('R5: KB IS CONSISTENT'), nl
    ),
    nl,
    write('--- Assumption Dependence Testing ---'), nl,
    forall(conclusion(Answer),
           forall(active_assumption(A),
                  (retract(active_assumption(A)),
                   (prove(conclusion(Answer), _) ->
                       write('ROBUST without '), write(A), nl
                   ;
                       write('DEPENDS on '), write(A), nl
                   ),
                   assertz(active_assumption(A))))).

:- main.
--- prolog output ---
R3: evidence ingested from 5+ authoritative sources
R4: derived 310 conclusion(s)
  Conclusion: scam_types_identified
    Proof: proved(conclusion(scam_types_identified))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: voice_cloning_is_key_threat
    Proof: proved(conclusion(voice_cloning_is_key_threat))
  Conclusion: voice_cloning_is_key_threat
    Proof: proved(conclusion(voice_cloning_is_key_threat))
  Conclusion: voice_cloning_is_key_threat
    Proof: proved(conclusion(voice_cloning_is_key_threat))
  Conclusion: voice_cloning_is_key_threat
    Proof: proved(conclusion(voice_cloning_is_key_threat))
  Conclusion: voice_cloning_is_key_threat
    Proof: proved(conclusion(voice_cloning_is_key_threat))
  Conclusion: voice_cloning_is_key_threat
    Proof: proved(conclusion(voice_cloning_is_key_threat))
  Conclusion: voice_cloning_is_key_threat
    Proof: proved(conclusion(voice_cloning_is_key_threat))
  Conclusion: voice_cloning_is_key_threat
    Proof: proved(conclusion(voice_cloning_is_key_threat))
  Conclusion: voice_cloning_is_key_threat
    Proof: proved(conclusion(voice_cloning_is_key_threat))
  Conclusion: regulatory_response_active
    Proof: proved(conclusion(regulatory_response_active))
  Conclusion: regulatory_response_active
    Proof: proved(conclusion(regulatory_response_active))
  Conclusion: regulatory_response_active
    Proof: proved(conclusion(regulatory_response_active))
  Conclusion: regulatory_response_active
    Proof: proved(conclusion(regulatory_response_active))
  Conclusion: regulatory_response_active
    Proof: proved(conclusion(regulatory_response_active))
  Conclusion: regulatory_response_active
    Proof: proved(conclusion(regulatory_response_active))
  Conclusion: regulatory_response_active
    Proof: proved(conclusion(regulatory_response_active))
  Conclusion: regulatory_response_active
    Proof: proved(conclusion(regulatory_response_active))
  Conclusion: regulatory_response_active
    Proof: proved(conclusion(regulatory_response_active))
  Conclusion: regulatory_response_active
    Proof: proved(conclusion(regulatory_response_active))
  Conclusion: regulatory_response_active
    Proof: proved(conclusion(regulatory_response_active))
  Conclusion: regulatory_response_active
    Proof: proved(conclusion(regulatory_response_active))
  Conclusion: regulatory_response_active
    Proof: proved(conclusion(regulatory_response_active))
  Conclusion: regulatory_response_active
    Proof: proved(conclusion(regulatory_response_active))
  Conclusion: regulatory_response_active
    Proof: proved(conclusion(regulatory_response_active))
  Conclusion: regulatory_response_active
    Proof: proved(conclusion(regulatory_response_active))
  Conclusion: regulatory_response_active
    Proof: proved(conclusion(regulatory_response_active))
  Conclusion: regulatory_response_active
    Proof: proved(conclusion(regulatory_response_active))
  Conclusion: regulatory_response_active
    Proof: proved(conclusion(regulatory_response_active))
  Conclusion: regulatory_response_active
    Proof: proved(conclusion(regulatory_response_active))
  Conclusion: regulatory_response_active
    Proof: proved(conclusion(regulatory_response_active))
  Conclusion: regulatory_response_active
    Proof: proved(conclusion(regulatory_response_active))
  Conclusion: regulatory_response_active
    Proof: proved(conclusion(regulatory_response_active))
  Conclusion: regulatory_response_active
    Proof: proved(conclusion(regulatory_response_active))
  Conclusion: regulatory_response_active
    Proof: proved(conclusion(regulatory_response_active))
  Conclusion: multi_billion_dollar_scale
    Proof: proved(conclusion(multi_billion_dollar_scale))
  Conclusion: multi_billion_dollar_scale
    Proof: proved(conclusion(multi_billion_dollar_scale))
  Conclusion: multi_billion_dollar_scale
    Proof: proved(conclusion(multi_billion_dollar_scale))
  Conclusion: multi_billion_dollar_scale
    Proof: proved(conclusion(multi_billion_dollar_scale))
  Conclusion: multi_billion_dollar_scale
    Proof: proved(conclusion(multi_billion_dollar_scale))
  Conclusion: multi_billion_dollar_scale
    Proof: proved(conclusion(multi_billion_dollar_scale))
  Conclusion: multi_billion_dollar_scale
    Proof: proved(conclusion(multi_billion_dollar_scale))
  Conclusion: multi_billion_dollar_scale
    Proof: proved(conclusion(multi_billion_dollar_scale))
  Conclusion: multi_billion_dollar_scale
    Proof: proved(conclusion(multi_billion_dollar_scale))
  Conclusion: multi_billion_dollar_scale
    Proof: proved(conclusion(multi_billion_dollar_scale))
  Conclusion: multi_billion_dollar_scale
    Proof: proved(conclusion(multi_billion_dollar_scale))
  Conclusion: multi_billion_dollar_scale
    Proof: proved(conclusion(multi_billion_dollar_scale))
  Conclusion: multi_billion_dollar_scale
    Proof: proved(conclusion(multi_billion_dollar_scale))
  Conclusion: multi_billion_dollar_scale
    Proof: proved(conclusion(multi_billion_dollar_scale))
  Conclusion: multi_billion_dollar_scale
    Proof: proved(conclusion(multi_billion_dollar_scale))
  Conclusion: multi_billion_dollar_scale
    Proof: proved(conclusion(multi_billion_dollar_scale))
  Conclusion: multi_billion_dollar_scale
    Proof: proved(conclusion(multi_billion_dollar_scale))
  Conclusion: multi_billion_dollar_scale
    Proof: proved(conclusion(multi_billion_dollar_scale))
  Conclusion: multi_billion_dollar_scale
    Proof: proved(conclusion(multi_billion_dollar_scale))
  Conclusion: multi_billion_dollar_scale
    Proof: proved(conclusion(multi_billion_dollar_scale))
  Conclusion: multi_billion_dollar_scale
    Proof: proved(conclusion(multi_billion_dollar_scale))
  Conclusion: multi_billion_dollar_scale
    Proof: proved(conclusion(multi_billion_dollar_scale))
  Conclusion: multi_billion_dollar_scale
    Proof: proved(conclusion(multi_billion_dollar_scale))
  Conclusion: multi_billion_dollar_scale
    Proof: proved(conclusion(multi_billion_dollar_scale))
  Conclusion: multi_billion_dollar_scale
    Proof: proved(conclusion(multi_billion_dollar_scale))
  Conclusion: ai_lowers_barrier_to_entry
    Proof: proved(conclusion(ai_lowers_barrier_to_entry))
  Conclusion: ai_lowers_barrier_to_entry
    Proof: proved(conclusion(ai_lowers_barrier_to_entry))
  Conclusion: ai_lowers_barrier_to_entry
    Proof: proved(conclusion(ai_lowers_barrier_to_entry))
  Conclusion: ai_lowers_barrier_to_entry
    Proof: proved(conclusion(ai_lowers_barrier_to_entry))
  Conclusion: ai_lowers_barrier_to_entry
    Proof: proved(conclusion(ai_lowers_barrier_to_entry))
  Conclusion: ai_lowers_barrier_to_entry
    Proof: proved(conclusion(ai_lowers_barrier_to_entry))
  Conclusion: ai_lowers_barrier_to_entry
    Proof: proved(conclusion(ai_lowers_barrier_to_entry))
  Conclusion: ai_lowers_barrier_to_entry
    Proof: proved(conclusion(ai_lowers_barrier_to_entry))
  Conclusion: ai_lowers_barrier_to_entry
    Proof: proved(conclusion(ai_lowers_barrier_to_entry))
  Conclusion: institutional_fraud_enabled
    Proof: proved(conclusion(institutional_fraud_enabled))
  Conclusion: institutional_fraud_enabled
    Proof: proved(conclusion(institutional_fraud_enabled))
  Conclusion: institutional_fraud_enabled
    Proof: proved(conclusion(institutional_fraud_enabled))
  Conclusion: institutional_fraud_enabled
    Proof: proved(conclusion(institutional_fraud_enabled))
  Conclusion: institutional_fraud_enabled
    Proof: proved(conclusion(institutional_fraud_enabled))
  Conclusion: institutional_fraud_enabled
    Proof: proved(conclusion(institutional_fraud_enabled))
  Conclusion: institutional_fraud_enabled
    Proof: proved(conclusion(institutional_fraud_enabled))
  Conclusion: institutional_fraud_enabled
    Proof: proved(conclusion(institutional_fraud_enabled))
  Conclusion: institutional_fraud_enabled
    Proof: proved(conclusion(institutional_fraud_enabled))
  Conclusion: institutional_fraud_enabled
    Proof: proved(conclusion(institutional_fraud_enabled))
  Conclusion: institutional_fraud_enabled
    Proof: proved(conclusion(institutional_fraud_enabled))
  Conclusion: institutional_fraud_enabled
    Proof: proved(conclusion(institutional_fraud_enabled))
  Conclusion: institutional_fraud_enabled
    Proof: proved(conclusion(institutional_fraud_enabled))
  Conclusion: institutional_fraud_enabled
    Proof: proved(conclusion(institutional_fraud_enabled))
  Conclusion: institutional_fraud_enabled
    Proof: proved(conclusion(institutional_fraud_enabled))
  Conclusion: institutional_fraud_enabled
    Proof: proved(conclusion(institutional_fraud_enabled))
R5: KB IS CONSISTENT

--- Assumption Dependence Testing ---
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
ROBUST without sources_authoritative
ROBUST without scam_classification_complete
- Retrieving artifact: artifact_fe06f8372caf
- [OK] Artifact artifact_fe06f8372caf -- prolog_exec: prolog_exec: 
%% --- Harness ---
:- dynamic active_assumption/1.

prove(G (31087 chars)

R3: evidence ingested from 5+ authoritative sources
R4: derived 310 conclusion(s)
  Conclusion: scam_types_identified
    Proof: proved(conclusion(scam_types_identified))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is_scaling_factor
    Proof: proved(conclusion(ai_is_scaling_factor))
  Conclusion: ai_is
- Synthesizing final answer
- Groundedness check: all 17 factual claims matched structured observations or raw tool evidence.

## Thinking

The user is asking about latest scams affecting Australia involving AI. This is a current affairs / factual query about real-world events. The question asks about "latest" scams, which means I need current information. This falls under the REASON tier (it's a factual lookup / current events question, not primarily mathematical or code-based).

Let me first check for premise defects:
- The question asks about "latest scams affecting Australia involving AI" - this seems well-posed. There's no false dichotomy, category error, self-referential paradox, undefined term, or fatal ambiguity. The presupposition that scams involving AI exist and affect Australia is plausible and testable.
- No premise defect found.

The injected triage is REASON. I need to follow the REASON workflow: R1 specify, R2 acquire (web_search), R3 ingest, R4 derive, R5 check, R6 validate, R7 answer.

Let me start with R1 - specify what I need. Since this is about current events, I need web_lookup capability.

Let me first do R1 (specify with prolog_exec), then do the web search.

Actually, let me just start with the web search since the need is clear - I need current information about AI scams in Australia. Let me do R1 first though.

Let me follow the workflow properly.Good. R1 is done. Now R2 - acquire. Let me search for current information on AI scams in Australia.I have good results. Let me also browse the ABC News article and the ASIC media release for more detail, and search for a few more specific scam types.Let me browse a couple more key articles and also look for specific types of AI scams like deepfake celebrity endorsements and the job scams mentioned.Let me also look for the job scam and romance scam information, and then also look for more about the "pig butchering" / romance scams using AI.I have quite a bit of information now. Let me also browse a couple more key sources, particularly the ASIC media release and the Westpac warning.Now I have sufficient evidence. Let me also quickly search for the Westpac warning and the Commonwealth Bank AI loan fraud mention.Good, I have enough evidence now. Let me proceed with R3 (ingest) and R4 (derive) in Prolog. Let me now build the substantive REASON program.

Key facts I've gathered:

1. ASIC (April 2026): AI supercharging online scams. 11,964 scam sites removed in 2025 (90% increase). 1,100+ social media ads taken down. $2.18 billion lost to scams in 2025 ($837.7m investment scams).

2. AI Voice Cloning (Swinburne University, Feb 2026): $25.8m lost in first half of 2025 alone. Scammers use generative AI to clone voices from social media. Impersonate family members ("Hi Mum" scam), bosses, partners.

3. Deepfake Celebrity Endorsements: AI-generated videos of well-known Australians (business figures, TV personalities) promoting fake investment platforms on Facebook, Instagram, YouTube.

4. AI-Powered Phishing: AI generates polished, personalized phishing emails referencing real names, banks, recent transactions. No more typos - looks exactly like official bank communications.

5. Property/Loan Fraud: Commonwealth Bank alerted authorities (early 2026) about suspected $1 billion loan fraud racket where AI generated fake financial documents for home loans.

6. Job Scams: AI-generated job ads targeting young people, often used for money laundering / "money mule" recruitment.

7. Pig Butchering / Romance Scams: AI chatbots used to build trust over weeks/months before asking for money.

8. "Cloaking": Scammers use AI to hide content that violates platform terms, showing different content based on device/location.

9. Scale: AI allows spinning up 100+ websites instantly. Professor Paul Haskell-Dowland (ECU): AI has made scams go from "spot them a mile off" to highly convincing.

10. Regulatory response: ASIC's takedown service, Scamwatch warnings, National Anti-Scam Centre.

Let me now create the Prolog program.The output got large because of the multiple acquired facts causing explosion of conclusions. Let me check the full output to see if the dependence testing worked properly. Let me retrieve the artifact.The Prolog derivation worked correctly. The conclusions derived are:

1. scam_types_identified - 8 types identified
2. ai_is_scaling_factor - AI is a scaling factor for scams
3. voice_cloning_is_key_threat - Voice cloning is a key threat
4. regulatory_response_active - ASIC actively responding
5. multi_billion_dollar_scale - $2.18 billion lost
6. ai_lowers_barrier_to_entry - AI lowers barriers
7. institutional_fraud_enabled - AI enabling institutional-level fraud

The KB is consistent. All conclusions are ROBUST against both assumptions (since the conclusions are based on hard acquired facts, not assumptions). 

Now I need to proceed to R6 (validate) and R7 (answer). All spec requirements are fulfilled:
- identify_scams: 8 scam types listed ✓
- describe_methods: each scam type described ✓
- cite_sources: ASIC, ABC News, Swinburne, ACCC cited ✓
- temporal: all sources from 2025-2026 ✓

Now I'll write the final answer.

## Final Answer

As of mid-2026, AI is "supercharging" scams targeting Australians at an unprecedented scale. Australians lost **$2.18 billion** to scams in 2025 (National Anti-Scam Centre), with investment scams alone accounting for **$837.7 million**. ASIC removed a record **11,964** phishing and investment scam websites in 2025 — a 90% increase from the prior year. The eight major AI-enabled scam categories identified are:

1. **AI Deepfake Celebrity Investment Ads** — AI-cloned faces/voices of Australian celebrities in fake investment videos on social media
2. **AI Voice Cloning ("Hi Mum" / Family Emergency)** — AI replicates a family member's voice from social media audio clips; $25.8 million lost in H1 2025 alone
3. **AI-Powered Phishing Emails & SMS** — Perfectly written, personalized messages referencing real names, banks, and transactions
4. **AI-Generated Fake Investment Platforms & Trading Bots** — Polished websites falsely claiming AI trading bots generate guaranteed high returns
5. **AI-Facilitated Loan & Property Fraud** — AI-generated fake financial documents for fraudulent loan applications (CBA flagged a suspected $1 billion racket)
6. **AI-Powered Romance / Pig Butchering Scams** — AI chatbots build romantic trust over weeks/months, then direct victims to fake investment platforms
7. **AI-Generated Job Scams & Money Mule Recruitment** — Convincing fake job ads targeting young people to share bank details or launder money
8. **AI Cloaking & Platform Evasion** — AI hides scam content from platform moderators by showing different content based on device/location

Regulators (ASIC, ACCC's National Anti-Scam Centre, Scamwatch) are actively responding, but as ECU Professor Paul Haskell-Dowland noted, AI has turned cybercrime into a "supermarket aisle" where scammers can spin up 100 convincing websites "at the flick of a switch."

- **Problem**: Identify the latest scams involving artificial intelligence affecting Australians (as of mid-2026).
- **Requirements**:
  - List specific AI-enabled scam types targeting Australians
  - Describe how AI is used in each scam type
  - Provide recent authoritative sources
  - Focus on latest/recent scams (2025–2026)

---
Finished: `2026-07-22T02:51:24`
