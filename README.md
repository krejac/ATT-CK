![](./ku-attack.png)

---

## Kort intro til ATT&CK

[Mitre](https://mitre.org/) er en ikke-for-profit organisation, der ”løser problemer for at sikre verdenen”[^1], som har lavet og vedligeholder ATT&CK frameworket, som systematisk sætter avancerede hackergrupperingers taktikker og teknikker ind i en ramme, så it-sikkerhedsfolk kan se hvad man bør holde styr på i et it-miljø.

*ATT&CK* er et akronym for *Advanced Tactics, Techniques & Common Knowledge*.

*Tactics* er målet for en given handling.

*Techniques* er metoden til at opnå målet.

Grunden til at det er smart at bruge et framework som ATT&CK kan ses, hvis man kigger på [Pyramid of Pain](http://detect-respond.blogspot.com/2013/03/the-pyramid-of-pain.html), som beskriver hvor svært det er for en angriber at ændre forskellige "Indicators of Compromise" (IoC).

![Pyramid of Pain](./Pyramid%20of%20Pain%20v2.png)

Det Pyramid of Pain viser er, at hvis ens metode til at opdage angreb er baseret på de IoC'ere vi ser i bunden at pyramiden er det trivielt for angriberne at ændre mønster, så de undslipper opdagelse, men jo højere op ad pyramiden man klatrer, desto sværre er det - for angriber - at ændre signaturen. 

ATT&CK sigter mod "Tools Techniques and Procedures" (TTP) i toppen af figuren og kan man opdage dem, gør man det for alvor svært at forblive uset som angriber.

## Kom i gang med Mitres ATT&CK framework

Bedste sted at få en masse info om ATT&CK er via Mitres forskellige sider online. Her kan man finde bl.a. [papers](https://www.mitre.org/publication-keywords/computer-security) samt [blog posts](https://medium.com/mitre-attack) og [videoer](https://www.youtube.com/watch?v=yslLIqfOKCU&list=PLkTApXQou_8JrhtrFDfAskvMqk97Yu2S2).

### Læsning

Hurtigt overblik over hovedpointer om ATT&CK:   
- [ATT&CK 101 Blog Post](https://medium.com/mitre-attack/att-ck-101-17074d3bc62)

#### Kom i gang blogposts fra Mitre:
Kan med fordel læses i denne rækkefølge.

1.	[Getting Started with ATT&CK: Threat Intelligence](https://medium.com/mitre-attack/getting-started-with-attack-cti-4eb205be4b2f)
2.	[Getting Started with ATT&CK: Detection and Analytics](https://medium.com/mitre-attack/getting-started-with-attack-detection-a8e49e4960d0)
3.	[Getting Started with ATT&CK: Adversary Emulation and Red Teaming](https://medium.com/mitre-attack/getting-started-with-attack-red-29f074ccf7e3)
4.	[Getting Started with ATT&CK: Assessments and Engineering](https://medium.com/mitre-attack/getting-started-with-attack-assessment-cc0b01769cb4)

Se også ATT&CK-hjemmesidens [Getting Started](https://attack.mitre.org/resources/getting-started/) afsnit for yderligere ressourcer.

### Videoer

<center><iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/0BEf6s1iu5g" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center>

<center><iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/bkfwMADar0M" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center>
Bemærk evt. top 20 techniques ved ~31:30.

Hvordan kan ATT&CK konkret anvendes i et SIEM?
- [MITRE ATT&CKcon 2018: Summiting the Pyramid of Pain: Operationalizing ATT&CK](https://www.youtube.com/watch?v=YhsN5pBDrGY) (~30:00)
- [MITRE ATT&CKcon 2018: From Technique to Detection](https://www.youtube.com/watch?v=a3hIIzJrH14) (~5:00)
- [Building The MITRE ATT&CK Technique Detection into Your Security Monitoring](https://www.brighttalk.com/webcast/14907/366642) (~1:00:00)

## Ideer til hvordan man kan komme i gang
(Løst baseret på tanker i bogen A Data-Driven Computer Defence af Roger A. Grimes)

1. Identificer de vigtigste _succesfulde_ nuværende angreb (5-10stk).
2. Identificer de vigtigste _potentielle_ fremtidige angreb (5-10stk).
3. Find metrikker til at måle de i 1+2 identificerede angreb.
4. Ranger de i 3 _målte_ angreb baseret på hyppighed / alvorlighed.
5. Arbejd på at mitigere værste trussel først indtil den ikke længere er værst mere.
6. [goto 5.]
7. Periodevis vurderes lister fra 1+2.



## Yderligere ressourcer / værktøjer
ATT&CK:
- [Hjemmeside](https://attack.mitre.org/)
- [ATT&CK Navigator](https://mitre-attack.github.io/attack-navigator/enterprise/) ([om navigatoren](https://www.mitre.org/capabilities/cybersecurity/overview/cybersecurity-blog/the-attck%E2%84%A2-navigator-a-new-open-source))
- [MITRE Cyber Analytics Repository](https://car.mitre.org/) (Voksende bibliotek af "detection techniques")
- [MITREblog: ATT&CK Sub-Techniques Preview](https://medium.com/mitre-attack/attack-sub-techniques-preview-b79ff0ba669a)

Log Management:
- [NIST] [Guide to Computer Security Log Management](https://csrc.nist.gov/publications/detail/sp/800-92/final)

Andre relevante modeller:
- [Cyber Kill Chain](https://www.lockheedmartin.com/en-us/capabilities/cyber/cyber-kill-chain.html) fra Lockheed Martin. God, når man skal forklare et angrebs anatomi til ledelsen.
- [Pyramid of Pain](http://detect-respond.blogspot.com/2013/03/the-pyramid-of-pain.html). God, når man skal forstå hvorfor vi bruger ATT&CK.

Test af Detection Techniques:
- Brug [Atomic Red Team](https://atomicredteam.io/testing) til automatisering af red team testing.

Artikler:
- [Getting Started with ATT&CK? New Report Suggests Prioritizing PowerShell](https://redcanary.com/blog/getting-started-with-attck-new-report-suggests-prioritizing-powershell/)
- [Four tools to consider if you're adopting ATT&CK](https://redcanary.com/blog/four-tools-to-consider-if-youre-adopting-attck/)
- [ATT&CK™ Is Only as Good as Its Implementation: Avoiding Five Common Pitfalls](https://redcanary.com/blog/avoiding-common-attack-pitfalls/)


## Nyttige forkortelser og Begreber

**APT** - Advanced Persistent Threat   
**ATT&CK** - Adversarial Tactics Techniques & Common Knowledge   
**CTI** - Cyber Threat Intelligence   
**CVE** - Common Vulnerabilities and Exposures   
**IOC** - Indicator of Compromise   
**SIEM** - Security Information and Event Management   
**SOC** - Security Operation Center   
**TTPs** - Tactics, Techniques, and Procedures   

Se flere på [Cybersecurity Dictionary](https://www.optiv.com/cybersecurity-dictionary).

[^1]: Ref.: [Corporate Overview](https://www.mitre.org/about/corporate-overview) (mitre.org)
