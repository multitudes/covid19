---
title: Covid-19, Ihre Gemeinschaft und Sie - eine datenwissenschaftliche Perspektive
date:   2020-03-10 09:38
tags: Data Science, FastAI, Translation 
excerpt: Covid-19, Ihre Gemeinschaft und Sie - eine datenwissenschaftliche Perspektive - Übersetzung des Artikels von Jeremy Howard und Rachel Thomas ins Deutsche
---
Geschrieben: 09 Mar 2020 von Jeremy Howard und Rachel Thomas

<style type="text/css">
blockquote {
    color: #7a7a7a;
    border-left: .25rem solid #e5e5e5;
    margin: .8 rem 0px;
    padding-right: 5rem;
    padding-left: 1.25rem;
}
a { 
color: #268bd2;
}
</style>

> Wir sind Datenwissenschaftler - das heißt, es ist unsere Aufgabe, zu verstehen, wie man Daten analysiert und interpretiert. Wenn wir die Daten um Covid-19 analysieren, sind wir sehr besorgt.  Die anfälligsten Schichten der Gesellschaft, die Älteren und die Armen, sind am stärksten gefährdet, aber die Kontrolle der Ausbreitung und der Auswirkungen der Krankheit erfordert von uns allen eine Verhaltensänderung. Waschen Sie Ihre Hände gründlich und regelmäßig, vermeiden Sie Gruppen und Menschenansammlungen, sagen Sie Veranstaltungen ab und berühren Sie nicht Ihr Gesicht. In diesem Beitrag erklären wir, warum wir besorgt sind, und Sie sollten es auch sein. Für eine sehr gute Zusammenfassung der wichtigsten Informationen, bitte lesen Sie [Corona in Brief](https://docs.google.com/document/u/1/d/1vumYWoiV7NlVoc27rMQvmVkVu5cOAbnaW_RKkq2RMaQ/mobilebasic?fbclid=IwAR0If1zzDDldgAy3DZmFhaxAmP046-dwAE_LCj3l9su2XLYpZe2By8mCj1A) von Ethan Alley (Präsident einer gemeinnützigen Organisation, die Technologien zur Verringerung der Risiken von Pandemien entwickelt).

## Übersetzungen

Jeder ist willkommen, diesen Artikel zu übersetzen, um seinen lokalen Gemeinschaften zu helfen, diese Themen zu verstehen. Bitte verlinken Sie mit entsprechendem Vermerk auf diese Seite zurück. Lassen Sie es uns auf [Twitter](https://twitter.com/jeremyphoward) wissen, damit wir Ihre Übersetzung in diese Liste aufnehmen können.

- [Französisch](https://medium.com/@xrb/covid-19-votre-communauté-et-vous-3e5f127910bc)
- [Spanisch](https://datus.encryptedcommerce.net/public-health/2020/03/09/Covid-19-datascience-translation.html)
- [Portugiesisch (Brasilien)](https://medium.com/@gpalmape/covid-19-sua-comunidade-e-você-uma-perspectiva-de-ciência-de-dados-cbdded20e436)
- [Thailändisch](https://medium.com/mmaetha/covid-19-สังคม-และตัวคุณเอง-ในมุมมองของวิทยาศาสตร์ข้อมูล-1323c34fd4df)
- [Deutsch](https://multitudes.github.io/posts/Covid19/)

## Inhalt

- <a href="#system">Wir brauchen ein funktionierendes medizinisches System</a>
- <a href="#grippe">Dies ist nicht wie die Grippe</a>
- <a href="#panik">"Keine Panik. Ruhe bewahren" ist nicht hilfreich</a>
- <a href="#sie">Es geht nicht nur um Sie</a>
- <a href="#kurve">Wir müssen die Kurve abflachen</a>
- <a href="#react">Die Reaktion einer Gemeinschaft macht den Unterschied</a>
- <a href="#usa">Wir haben keine guten Informationen in den USA</a>
- <a href="#end">Zum Schluss</a>


<h2 id='system'>Wir brauchen ein funktionierendes medizinisches System</h2>

Vor etwas mehr als 2 Jahren bekam eine von uns (Rachel) eine Hirninfektion, an der etwa 1/4 der Betroffenen stirbt und 1/3 mit einer dauerhaften kognitiven Beeinträchtigung zurückbleibt. Viele andere enden mit dauerhaften Seh- und Hörschäden. Rachel war im Delirium, als sie über den Krankenhausparkplatz kroch. Sie hatte das Glück, eine schnelle Behandlung, Diagnose und Betreuung zu erhalten. Bis kurz vor diesem Ereignis war Rachel bei bester Gesundheit. Der sofortige Zugang zur Notaufnahme hat ihr mit ziemlicher Sicherheit das Leben gerettet.

Lassen Sie uns nun über Covid-19 sprechen und darüber, was in den kommenden Wochen und Monaten mit den Leuten in Rachels Situation geschehen könnte. Die Zahl der Menschen, die mit Covid-19 infiziert sind, verdoppelt sich alle 3 bis 6 Tage. Bei einer Verdoppelungsrate von drei Tagen bedeutet das, dass die Zahl der Menschen, die sich infiziert haben, innerhalb von drei Wochen um das 100-fache ansteigen kann (das ist eigentlich nicht ganz so einfach, aber lassen wir uns nicht von technischen Details ablenken). Eine von 10 infizierten Personen muss für viele Wochen ins Krankenhaus eingeliefert werden, und die meisten benötigen Sauerstoff. Obwohl es für dieses Virus noch sehr früh ist, gibt es bereits Regionen, in denen die Krankenhäuser völlig überfüllt sind und die Menschen nicht mehr in der Lage sind, die erforderliche Behandlung zu erhalten (nicht nur für Covid-19, sondern auch für alles andere, wie z.B. die lebensrettende Behandlung, die Rachel brauchte). In Italien zum Beispiel, wo noch vor einer Woche Beamte sagten, dass alles in Ordnung sei, sind jetzt sechzehn Millionen Menschen isoliert worden (<em>Update: 6 Stunden nach der Veröffentlichung des Artikels hat Italien das ganze Land isoliert</em>), und es werden Zelte wie dieses aufgebaut, um den Zustrom von Patienten zu bewältigen:


<p align="center">
  <img src="https://www.fast.ai/images/coronavirus/image1.jpeg" class="pure-img-responsive" title="Ein medizinisches Zelt in Italien"></img>
  <caption>Ein medizinisches Zelt in Italien</caption>
</p>

Dr. Antonio Pesenti, Leiter des regionalen Krisenreaktionskommandos in einem schwer betroffenen Gebiet Italiens, [sagte][12]: "Wir sind jetzt gezwungen, eine Intensivbehandlung in Korridoren, in Operationssälen, in Erholungsräumen einzurichten... Eines der besten Gesundheitssysteme der Welt, in der Lombardei, ist einen Schritt vom Zusammenbruch entfernt".

<h2 id='grippe'>Dies ist nicht wie die Grippe</h2>

Die Grippe hat eine Todesrate von etwa 0,1% der Infektionen. Marc Lipsitch, der Direktor des "Center for Communicable Disease Dynamics" in Harvard, [schätzt](https://www.washingtonpost.com/opinions/2020/03/06/why-its-so-hard-pin-down-risk-dying-coronavirus/), dass sie bei Covid-19 bei 1-2% liegt. Die jüngste [epidemiologische Modellierung](https://www.medrxiv.org/content/10.1101/2020.03.04.20031104v1.full.pdf) ergab im Februar eine Rate von 1,6% in China, sechzehnmal höher als bei der Grippe<sup id="fnref:epid"><a class="footnote" href="#fn:epid">1</a></sup> (dies könnte jedoch eine recht konservative Zahl sein, da die Raten stark ansteigen, wenn das medizinische System nicht mehr ausreicht). Die derzeit besten Schätzungen gehen davon aus, dass Covid-19 in diesem Jahr zehnmal mehr Menschen töten wird als die Grippe (und [die Modellierung von Elena Grewal](https://docs.google.com/spreadsheets/d/1ktSfdDrX_uJsdM08azBflVOm4Z5ZVE75nA0lGygNgaA/edit?usp=sharing), der ehemaligen Direktorin für Datenwissenschaft bei Airbnb, zeigt, dass es im schlimmsten Fall 100 Mal mehr sein könnten). Dies ist vor Berücksichtigung der enormen Auswirkungen auf das medizinische System, wie sie oben beschrieben wurden. Es ist verständlich, dass einige Leute versuchen, sich davon zu überzeugen, dass eine Krankheit ähnlich der Grippe nichts Neues ist, denn es ist sehr unangenehm zu akzeptieren, dass wir über diese Krankheit zu wenig wissen.

Der Versuch, intuitiv zu verstehen, dass die Zahl der Infizierten exponentiell zunimmt, ist nicht etwas, für das unser Gehirn ausgelegt ist. Wir müssen also die Daten als Wissenschaftler analysieren und nicht nur unserer Intuition vertrauen.

<p align="center">
  <img src="https://www.fast.ai/images/coronavirus/image2.png" class="pure-img-responsive" title="Total cases outside of China"></img>
  <caption>Wie wird dies in 2 Wochen aussehen? In 2 Monaten?</caption>
</p>

Für jede Person, die die Grippe hat, werden im Durchschnitt 1,3 andere Menschen infiziert. Das nennt man das "R0" für Grippe. Wenn R0 weniger als 1,0 beträgt, hört eine Infektion auf, sich auszubreiten und stirbt aus. Wenn sie über 1,0 liegt, breitet sie sich aus. R0 liegt derzeit bei 2-3 für Covid-19 außerhalb Chinas. Der Unterschied mag zwar klein klingen, aber nach 20 "Generationen" von Infizierten, die ihre Infektion weitergeben, würde ein R0 von 1,3 zu 146 Infektionen führen, aber ein R0 von 2,5 würde 36 Millionen Infektionen zur Folge haben! (Dies ist natürlich sehr schwankend) und ignoriert viele Auswirkungen in der realen Welt, aber es ist ein vernünftiges Beispiel für den relativen Unterschied zwischen Covid-19 und Grippe, wobei alle anderen Dinge gleich sind.

Beachten Sie, dass R0 nicht irgendeine grundlegende Eigenschaft einer Krankheit ist. Sie hängt stark von der Reaktion ab und kann sich im Laufe der Zeit ändern<sup id="fnref:r0"><a class="footnote" href="#fn:r0">2</a></sup>. Vor allem in China ist R0 für Covid-19 stark zurückgegangen und nähert sich jetzt dem Wert 1,0! Wie, fragen Sie? Indem man Maßnahmen in einem Ausmaß ergreift, das in einem Land wie den USA schwer vorstellbar wäre - zum Beispiel durch die vollständige Absperrung vieler Riesenstädte und die Entwicklung eines Testverfahrens, das es ermöglicht, mehr als eine Million Menschen pro Woche zu testen.

Eine Sache, die in den sozialen Netzwerken (auch von stark verfolgten Accounts wie Elon Musk) häufig vorkommt, ist ein Missverständnis des Unterschieds zwischen logistischem und exponentiellem Wachstum. Das "logistische" Wachstum bezieht sich auf das "s-förmige" Wachstumsmuster der sich in der Praxis ausbreitenden Epidemie. Offensichtlich kann ein exponentielles Wachstum nicht ewig anhalten, da sonst mehr Menschen infiziert würden als in der Welt! Daher müssen die Infektionsraten letztendlich immer abnehmen, was zu einer s-förmigen (als sigmoid bezeichneten) Wachstumsrate im Laufe der Zeit führt. Das abnehmende Wachstum tritt jedoch nur aus einem Grund auf - es ist keine Zauberei. Die Hauptgründe sind:

- Massive und effektive gemeinschaftliche Reaktion, oder
- Ein so großer Prozentsatz der Menschen ist infiziert, dass es weniger nicht infizierte Menschen gibt, auf die man sich ausbreiten kann.

Daher macht es keinen logischen Sinn, sich auf das logistische Wachstumsmuster zu verlassen, um eine Pandemie "unter Kontrolle" zu bringen.

Eine weitere Sache, die es schwierig macht, die Auswirkungen von Covid-19 in Ihrer lokalen Gemeinschaft intuitiv zu verstehen, ist die Tatsache, dass zwischen der Infektion und dem Krankenhauseinweisung eine sehr bedeutende Verzögerung liegt - im Allgemeinen etwa 11 Tage. Das mag nicht lange erscheinen, aber wenn man es mit der Anzahl der in dieser Zeit infizierten Menschen vergleicht, bedeutet es, dass die Infektion in der Gemeinschaft bereits so weit fortgeschritten ist, dass es 5-10 Mal mehr Menschen gibt, die behandelt werden müssen, wenn man merkt, dass die Krankenhäuser voll sind.

Beachten Sie, dass es einige frühe Anzeichen dafür gibt, dass die Auswirkungen in Ihrer Region zumindest etwas vom Klima abhängen könnten. Das Papier [Temperatur- und Breitenanalyse zur Vorhersage der potenziellen Ausbreitung und Saisonalität von COVID-19](https://poseidon01.ssrn.com/delivery.php?ID=091071099092098096101097074089104068104013035023062021010031112088025099126064001093097030102106046016114116082016095089113023126034089078012119081090111118122007110026000085123071022022127025026080005029001020025126022000066075021086079031101116126112&EXT=pdf) weist darauf hin, dass sich die Krankheit bisher in milden Klimazonen ausgebreitet hat (leider liegt der Temperaturbereich in San Francisco, wo wir leben, genau in diesem Bereich; er umfasst auch die wichtigsten Bevölkerungszentren Europas, einschließlich London).

<h2 id='panik'>"Keine Panik. Ruhe bewahren" ist nicht hilfreich.</h2>

Eine häufige Reaktion, die wir in den sozialen Medien auf Menschen gesehen haben, die auf die Gründe für ihre Besorgnis hinweisen, ist "Keine Panik" oder "Ruhe bewahren". Dies ist, um es milde auszudrücken, nicht hilfreich. Niemand behauptet, dass Panik eine angemessene Reaktion sei. Aus irgendeinem Grund ist "Ruhe bewahren" jedoch eine sehr beliebte Reaktion in bestimmten Kreisen (aber nicht bei den Epidemiologen, deren Aufgabe es ist, diese Dinge zu verfolgen). Vielleicht hilft "Ruhe bewahren" einigen Menschen, sich besser über ihre eigene Untätigkeit zu fühlen, oder sie fühlen sich irgendwie überlegen gegenüber Menschen, von denen sie glauben, dass sie wie ein kopfloses Huhn herumlaufen.

Aber "Ruhe bewahren" kann leicht zu einem Versagen bei der Vorbereitung und Reaktion führen. In China wurden Zehnmillionen Menschen eingesperrt und zwei neue Krankenhäuser gebaut, bis sie die Statistiken erreicht hatten, die die USA jetzt haben. Italien hat zu lange gewartet, und gerade heute (Sonntag, 8. März) wurden 1492 neue Fälle und 133 neue Todesfälle gemeldet, obwohl 16 Millionen Menschen eingeschlossen wurden. Auf der Grundlage der besten Informationen, die wir zum jetzigen Zeitpunkt ermitteln können, befand sich Italien noch vor 2-3 Wochen in der gleichen Lage wie die USA und Großbritannien heute (in Bezug auf die Infektionsstatistik).

Beachten Sie, dass zu diesem Zeitpunkt fast alles über Covid-19 in der Luft liegt. Wir wissen nicht wirklich, wie schnell die Infektion verläuft oder wie hoch die Sterblichkeit ist, wir wissen nicht, wie lange es an der Oberfläche aktiv bleibt, wir wissen nicht, ob es unter warmen Bedingungen überlebt und sich ausbreitet. Alles, was wir haben, sind derzeit beste Vermutungen auf der Grundlage der besten Informationen, die die Menschen zusammenstellen können. Und denken Sie daran, dass die überwiegende Mehrheit dieser Informationen in China liegt, in chinesischer Sprache. Der beste Weg, die bisherigen Erfahrungen in China zu verstehen, ist derzeit die Lektüre des ausgezeichneten [Report of the WHO-China Joint Mission on Coronavirus Disease 2019](https://www.who.int/docs/default-source/coronaviruse/who-china-joint-mission-on-covid-19-final-report.pdf), der auf einer gemeinsamen Mission von 25 nationalen und internationalen Experten aus China, Deutschland, Japan, Korea, Nigeria, Russland, Singapur, den Vereinigten Staaten von Amerika und der Weltgesundheitsorganisation (WHO) beruht.

Wenn eine gewisse Unsicherheit besteht, dass es sich vielleicht nicht um eine globale Pandemie handelt und vielleicht alles vorbeigehen könnte, ohne dass das Krankenhauswesen zusammenbricht, bedeutet das nicht, dass die richtige Reaktion darin besteht, nichts zu tun. Das wäre enorm spekulativ und keine optimale Reaktion unter jedem Bedrohungsszenario. Es scheint auch äußerst unwahrscheinlich, dass Länder wie Italien und China große Teile ihrer Wirtschaft ohne guten Grund effektiv stilllegen würden. Es stimmt auch nicht mit den tatsächlichen Auswirkungen überein, die wir vor Ort in infizierten Gebieten sehen, in denen das medizinische System nicht in der Lage ist, damit umzugehen (Italien beispielsweise verwendet 462 Zelte für die "Pre-triage" und muss immer noch Patienten auf der Intensivstation [aus infizierten Gebieten umziehen](https://www.repubblica.it/cronaca/2020/03/08/news/coronavirus_situazione_italia-250665818/?ref=RHPPTP-BH-I250661466-C12-P5-S1.12-T1)).

Stattdessen besteht die durchdachte, vernünftige Reaktion darin, die von Experten empfohlenen Schritte zu befolgen, um die Verbreitung von Infektionen zu vermeiden:

- Vermeiden Sie große Gruppen und Menschenmengen.
- Ereignisse abbrechen
- Arbeit von zu Hause aus, wenn überhaupt möglich
- Waschen Sie Ihre Hände beim Kommen und Gehen von zu Hause und häufig bei der Arbeit.
- Vermeiden Sie es, Ihr Gesicht zu berühren, besonders wenn Sie sich außerhalb Ihres Hauses befinden (nicht einfach!).
- Desinfizieren Sie Oberflächen und Verpackungen (es ist möglich, dass das Virus 9 Tage lang auf Oberflächen aktiv bleibt, obwohl dies noch nicht sicher bekannt ist).

<h2 id='sie'>Es geht nicht nur um Sie</h2>

Wenn Sie unter 50 Jahre alt sind und keine Risikofaktoren wie ein geschwächtes Immunsystem, eine Herz-Kreislauf-Erkrankung, eine Vorgeschichte mit Rauchen in der Vergangenheit oder andere chronische Krankheiten haben, können Sie sich damit trösten, dass Covid-19 Sie wahrscheinlich nicht töten wird. Aber wie Sie darauf reagieren, ist immer noch sehr wichtig. Die Wahrscheinlichkeit, dass Sie sich infizieren, ist immer noch genauso groß, und wenn Sie es tun, ist die Wahrscheinlichkeit, dass Sie andere anstecken, genauso groß. Im Durchschnitt infiziert jede infizierte Person mehr als zwei weitere Personen, und sie werden infektiös, bevor sie Symptome zeigen. Wenn Sie Eltern haben, die Ihnen wichtig sind, oder Großeltern, und planen, Zeit mit ihnen zu verbringen, und später feststellen, dass Sie für die Ansteckung mit Covid-19 verantwortlich sind, wäre das eine schwere Belastung, mit der Sie leben müssten.

Selbst wenn Sie keinen Kontakt zu Menschen über 50 haben, ist es wahrscheinlich, dass Sie mehr Mitarbeiter und Bekannte mit chronischen Krankheiten haben, als Ihnen bewusst ist. [Forschungsergebnisse](https://www.talentinnovation.org/_private/assets/DisabilitiesInclusion_KeyFindings-CTI.pdf) zeigen, dass nur wenige Menschen ihre gesundheitlichen Probleme am Arbeitsplatz offenlegen, wenn sie es [aus Angst vor Diskriminierung](https://medium.com/@racheltho/the-tech-industry-is-failing-people-with-disabilities-and-chronic-illnesses-8e8aa17937f3) vermeiden können. Wir beide gehören zu den Hochrisikokategorien, aber viele Menschen, mit denen wir regelmäßig zu tun haben, haben dies vielleicht nicht gewusst.

Und natürlich geht es nicht nur um die Menschen in Ihrer unmittelbaren Umgebung. Dies ist eine höchst wichtige ethische Frage. Jede Person, die ihr Bestes tut, um zur Kontrolle der Verbreitung des Virus beizutragen, hilft ihrer gesamten Gemeinschaft, die Infektionsrate zu verlangsamen. Wie Zeynep Tufekci[ in Scientific American](https://blogs.scientificamerican.com/observations/preparing-for-coronavirus-to-strike-the-u-s/) schrieb: "Die Vorbereitung auf die fast unvermeidliche weltweite Verbreitung dieses Virus ... ist eine der pro-sozialen, altruistischen Dinge, die man tun kann". Sie fährt fort:

> Wir sollten uns vorbereiten, nicht weil wir uns persönlich gefährdet fühlen könnten, sondern damit wir dazu beitragen können, das Risiko für alle zu verringern. Wir sollten uns nicht vorbereiten, weil wir vor einem unkontrollierbaren Weltuntergangsszenario stehen, sondern weil wir jeden Aspekt dieses Risikos, dem wir als Gesellschaft ausgesetzt sind, verändern können. Richtig, Sie sollten sich vorbereiten, weil Ihre Nachbarn Sie brauchen, um sich vorzubereiten - vor allem Ihre älteren Nachbarn, Ihre Nachbarn, die in Krankenhäusern arbeiten, Ihre Nachbarn mit chronischen Krankheiten und Ihre Nachbarn, die vielleicht nicht die Mittel oder die Zeit haben, sich vorzubereiten, weil ihnen die Mittel oder die Zeit fehlen.

Dies hat uns persönlich beeinflusst. Der größte und wichtigste Kurs, den wir jemals bei fast.ai eingerichtet haben und der für uns den Höhepunkt jahrelanger Arbeit darstellt, sollte in einer Woche an der Universität von San Francisco beginnen. Letzten Mittwoch (4. März) haben wir die Entscheidung getroffen, das Ganze online zu verlegen. Wir waren einer der ersten großen Kurse, die online gingen. Warum haben wir das getan? Weil uns Anfang letzter Woche klar wurde, dass wir, wenn wir diesen Kurs durchführen, implizit Hunderte von Menschen dazu ermutigen würden, sich in einem geschlossenen Raum zu treffen, und zwar mehrere Male über einen mehrwöchigen Zeitraum hinweg. Gruppen in geschlossenen Räumen zusammenzubringen, ist das Schlimmste, was man tun kann. Wir fühlten uns ethisch verpflichtet, dafür zu sorgen, dass dies zumindest in diesem Fall nicht passiert. Es war eine herzzerreißende Entscheidung. Die Zeit, die wir direkt mit unseren Studenten verbrachten, war eine der größten Freuden und produktivsten Perioden jedes Jahres. Und wir hatten Studenten, die aus der ganzen Welt einfliegen wollten, die wir wirklich nicht im Stich lassen wollten<sup id="fnref:r0"><a class="footnote" href="#fn:letdown">3</a></sup>.

Aber wir wussten, dass es das Richtige war, denn sonst würden wir wahrscheinlich die Ausbreitung der Krankheit in unserer Gemeinde verstärken<sup id="fnref:r0"><a class="footnote" href="#fn:changes">4</a></sup>.

<h2 id='kurve'>Wir müssen die Kurve abflachen</h2>

Dies ist äußerst wichtig, denn wenn wir die Infektionsrate in einer Gemeinde verlangsamen können, dann geben wir den Krankenhäusern in dieser Gemeinde Zeit, sich sowohl um die infizierten Patienten als auch um die regelmäßige Patientenlast zu kümmern, die sie bewältigen müssen. Dies wird als "Abflachung der Kurve" beschrieben und in diesem illustrativen Schaubild deutlich dargestellt:


<p align="center">
  <img src="https://www.fast.ai/images/coronavirus/image3.jpeg" class="pure-img-responsive" title="Bleiben unter dieser gepunkteten Linie bedeutet alles"></img>
  <caption>Wir müssen unter dieser gepunkteten Linie bleiben</caption>
</p>


Farzad Mostashari, der ehemalige nationale Koordinator für Gesundheits-IT, erklärte dies: "Jeden Tag werden neue Fälle identifiziert, die keine Reisegeschichte oder Verbindung zu einem bekannten Fall haben, und wir wissen, dass diese wegen der Verzögerungen bei den Tests nur die Spitze des Eisbergs sind. Das bedeutet, dass in den nächsten zwei Wochen die Zahl der diagnostizierten Fälle explodieren wird... Der Versuch, eine Eindämmung zu erreichen, wenn sich die Bevölkerung exponentiell ausbreitet, ist so, als würde man sich darauf konzentrieren, die Funken zu löschen, wenn das Haus brennt. Wenn das passiert, müssen wir unsere Strategien auf Schutzmaßnahmen umstellen, um die Ausbreitung zu verlangsamen und die Auswirkungen auf die Gesundheitsversorgung zu reduzieren. Wenn wir die Ausbreitung der Krankheit so gering halten können, dass unsere Krankenhäuser die Belastung bewältigen können, dann können die Menschen Zugang zu einer Behandlung erhalten. Aber wenn die Fälle zu schnell kommen, dann werden diejenigen, die einen Krankenhausaufenthalt benötigen, diesen nicht bekommen.

So könnte die Kalkulation aussehen, so [Liz Specht](https://twitter.com/LizSpecht/status/1236095186737852416):

> In den USA gibt es etwa 2,8 Krankenhausbetten pro 1000 Menschen. Bei einer Bevölkerung von 330 Mio. Einwohnern sind dies ~1 Mio. Betten. Zu einem bestimmten Zeitpunkt sind bereits 65 % dieser Betten belegt. Damit bleiben landesweit etwa 330.000 Betten verfügbar (vielleicht etwas weniger zu dieser Jahreszeit mit regelmäßiger Grippesaison usw.). Vertrauen wir den Zahlen Italiens und gehen wir davon aus, dass etwa 10% der Fälle schwerwiegend genug sind, um einen Krankenhausaufenthalt zu erfordern. (Denken Sie daran, dass bei vielen Patienten der Krankenhausaufenthalt wochenlang dauert - mit anderen Worten, der Umsatz wird sehr langsam sein, da sich die Betten mit COVID19-Patienten füllen). Nach dieser Schätzung werden bis etwa 8. Mai alle offenen Krankenhausbetten in den USA gefüllt sein. (Dies sagt natürlich nichts darüber aus, ob diese Betten für die Isolierung von Patienten mit einem hoch infektiösen Virus geeignet sind). Wenn wir uns beim Bruchteil der schweren Fälle um den Faktor zwei irren, ändert sich die Zeitlinie der Bettsättigung nur um 6 Tage in beide Richtungen. Wenn 20% der Fälle einen Krankenhausaufenthalt erfordern, gehen uns die Betten bis zum 2. Mai aus. Wenn nur 5% der Fälle einen Krankenhausaufenthalt erfordern, können wir es bis zum 14. Mai schaffen. Bei 2,5% schaffen wir es bis zum 20. Mai. Dies setzt natürlich voraus, dass die Nachfrage nach Betten aus anderen (nicht-COVID19) Gründen nicht steigt, was eine zweifelhafte Annahme zu sein scheint. Mit zunehmender Belastung des Gesundheitssystems, Rx-Knappheit usw. können Menschen mit chronischen Krankheiten, die normalerweise gut behandelt werden, in schwere medizinische Notlagen geraten, die eine intensive Pflege und einen Krankenhausaufenthalt erfordern.

<h2 id='react'>Die Reaktion einer Gemeinschaft macht den Unterschied</h2>

Wie wir bereits diskutiert haben, ist diese Kalkulation keine Gewissheit - China hat bereits gezeigt, dass es möglich ist, die Ausbreitung durch extreme Maßnahmen zu reduzieren. Ein weiteres großartiges Beispiel für eine erfolgreiche Reaktion ist Vietnam, wo u.a. eine landesweite Werbekampagne (einschließlich eines eingängigen Liedes!) schnell die Reaktion der Gemeinde mobilisierte und dafür sorgte, dass die Menschen ihr Verhalten entsprechend anpassten.

Dies ist nicht nur eine hypothetische Situation - sie wurde bei der Grippepandemie von 1918 deutlich sichtbar. In den Vereinigten Staaten zeigten zwei Städte sehr unterschiedliche Reaktionen auf die Pandemie: Philadelphia ging mit einer riesigen Parade von 200.000 Menschen voran, um Geld für den Krieg zu sammeln. Aber St. Louis führte sorgfältig konzipierte Prozesse ein, um die sozialen Kontakte zu minimieren und so die Verbreitung des Virus einzudämmen, und sagte gleichzeitig alle Großveranstaltungen ab. So sah die Zahl der Todesfälle in jeder Stadt aus, wie in den [Proceedings of the National Academy of Sciences](https://www.pnas.org/content/104/18/7582) gezeigt wird:


<p align="center">
  <img src="https://www.fast.ai/images/coronavirus/image4.jpeg" class="pure-img-responsive" title="Auswirkungen der unterschiedlichen Reaktionen auf die Grippepandemie von 1918"></img>
  <caption>Auswirkungen der unterschiedlichen Reaktionen auf die Grippepandemie von 1918</caption>
</p>

Die Situation in Philadelphia wurde extrem schlimm und erreichte sogar einen Punkt, an dem [es nicht mehr genug Bestattungssärge oder Leichenhallen gab](https://www.history.com/news/spanish-flu-pandemic-dead), um die große Zahl der Grippetoten zu bewältigen.

Richard Besser, der während der H1N1-Pandemie 2009 amtierender Direktor der Centers for Disease Control and Prevention war, [sagt](https://www.washingtonpost.com/opinions/as-coronavirus-spreads-the-bill-for-our-public-health-failures-is-due/2020/03/05/9da09ed6-5f10-11ea-b29b-9db42f7803a7_story.html?utm_campaign=wp_week_in_ideas&utm_medium=email&utm_source=newsletter&wpisrc=nl_ideas), dass in den USA "das Risiko der Exposition und die Fähigkeit, sich und seine Familie zu schützen, unter anderem vom Einkommen, dem Zugang zur Gesundheitsversorgung und dem Einwanderungsstatus abhängt". Er weist darauf hin:

> Ältere und behinderte Menschen sind besonders gefährdet, wenn ihr tägliches Leben und ihre Unterstützungssysteme gestört werden. Diejenigen, die keinen einfachen Zugang zu medizinischer Versorgung haben, einschließlich ländlicher und einheimischer Gemeinschaften, könnten in Zeiten der Not mit enormen Entfernungen konfrontiert sein. Menschen, die auf engem Raum leben - ob in öffentlichen Wohnungen, Pflegeheimen, Gefängnissen, Notunterkünften oder sogar Obdachlose auf der Straße - können in Wellen leiden, wie wir bereits im Bundesstaat Washington gesehen haben. Und die Verwundbarkeit der Niedriglohn-Gigantenwirtschaft mit nicht bezahlten Arbeitnehmern und prekären Arbeitszeiten wird während dieser Krise für alle sichtbar sein. Fragen Sie die 60 Prozent der US-Arbeitskräfte, die auf Stundenbasis bezahlt werden, wie einfach es ist, in einem Moment der Not eine Auszeit zu nehmen.

Das US Bureau of Labor Statistics zeigt, dass [weniger als ein Drittel der Beschäftigten](https://www.bls.gov/opub/ted/2018/higher-wage-workers-more-likely-than-lower-wage-workers-to-have-paid-leave-benefits-in-2018.htm) im untersten Einkommensbereich Zugang zu bezahltem Krankenstand haben:


<p align="center">
  <img src="https://www.fast.ai/images/coronavirus/image5.png" class="pure-img-responsive" title="Die meisten armen Amerikaner sind nicht krankgeschrieben, müssen also zur Arbeit gehen."></img>
  <caption>Die meisten armen Amerikaner sind nicht krankgeschrieben, müssen also zur Arbeit gehen.</caption>
</p>

<h2 id='usa'>Wir haben keine guten Informationen in den USA</h2>

Eines der großen Probleme in den USA ist, dass nur sehr wenige Tests durchgeführt werden und dass die Testergebnisse nicht richtig weitergegeben werden, was bedeutet, dass wir nicht wissen, was tatsächlich geschieht. Scott Gottlieb, der frühere FDA-Beauftragte, erklärte, dass in Seattle bessere Tests durchgeführt wurden und wir dort eine Infektion sehen: "Der Grund dafür, dass wir schon früh von dem Ausbruch von Covid-19 in Seattle wussten, war die Arbeit unabhängiger Wissenschaftler zur Überwachung der Sentinel-Seuche. In anderen Städten wurde eine solche Überwachung nie ganz in Gang gesetzt. Daher sind andere US-Hot-Spots möglicherweise noch nicht vollständig entdeckt worden." Laut [The Atlantic](https://www.theatlantic.com/health/archive/2020/03/how-many-americans-have-been-tested-coronavirus/607597/) versprach Vizepräsident Mike Pence, dass "etwa 1,5 Millionen Tests" diese Woche zur Verfügung stehen würden, aber bisher wurden weniger als 2.000 Personen in den gesamten USA getestet. Robinson Meyer und Alexis Madrigal von The Atlantic beriefen sich dabei auf die Arbeit des [COVID Tracking Project](https://docs.google.com/spreadsheets/u/1/d/e/2PACX-1vRwAqp96T9sYYq2-i7Tj0pvTf6XVHjDSMIKBdZHXiCGGdNC0ypEU9NbngS8mxea55JuCFuua1MUeOj5/pubhtml), so Robinson Meyer und Alexis Madrigal von The Atlantic:

> Die Zahlen, die wir gesammelt haben, deuten darauf hin, dass die amerikanische Reaktion auf das Covid-19 und die von ihm verursachte Krankheit COVID-19 schockierend träge war, insbesondere im Vergleich zu anderen entwickelten Ländern. Die CDC bestätigte vor acht Tagen, dass das Virus in den Vereinigten Staaten in der Gemeinschaft übertragen wurde - dass es Amerikaner infizierte, die weder ins Ausland gereist waren noch mit anderen in Kontakt standen, die es hatten. In Südkorea wurden innerhalb einer Woche nach dem ersten Fall einer Gemeindeübertragung mehr als 66.650 Personen getestet, und es wurde schnell möglich, 10.000 Personen pro Tag zu testen.

Teil des Problems ist, dass dies zu einem politischen Thema geworden ist. Insbesondere Präsident Donald Trump hat deutlich gemacht, dass er "die Zahlen" (d.h. die Zahl der Infizierten in den USA) niedrig halten möchte. Dies ist ein Beispiel dafür, dass die Optimierung von Metriken die Erzielung guter Ergebnisse in der Praxis behindert. (Weitere Informationen zu diesem Thema finden Sie im Papier [The Ethics of Data Science: [TThe Problem with Metrics is a Fundamental Problem for AI](https://arxiv.org/abs/2002.08512)). [Jeff Dean, Leiter der KI bei Google, twitterte](https://twitter.com/JeffDean/status/1236489084870119427) seine Besorgnis über die Probleme der politisierten Desinformation:

> Als ich bei der WHO arbeitete, war ich Teil des Globalen AIDS-Programms (jetzt UNAIDS), das geschaffen wurde, um der Welt bei der Bekämpfung der HIV/AIDS-Pandemie zu helfen. Die Mitarbeiter dort waren engagierte Ärzte und Wissenschaftler, die sich intensiv mit der Bewältigung dieser Krise beschäftigten. In Krisenzeiten sind klare und genaue Informationen von entscheidender Bedeutung, um allen zu helfen, richtige und fundierte Entscheidungen darüber zu treffen, wie sie reagieren sollen (Regierungen von Ländern, Staaten und Gemeinden, Unternehmen, NGOs, Schulen, Familien und Einzelpersonen). Mit den richtigen Informationen und Richtlinien, um den besten medizinischen und wissenschaftlichen Experten zuzuhören, werden wir alle Herausforderungen wie die von HIV/AIDS oder COVID-19 bewältigen. Bei einer von politischen Interessen getriebenen Desinformation besteht die reale Gefahr, die Dinge noch viel schlimmer zu machen, wenn wir angesichts einer wachsenden Pandemie nicht schnell und entschlossen handeln und aktiv Verhaltensweisen fördern, die die Krankheit tatsächlich schneller verbreiten. Diese ganze Situation ist unglaublich schmerzhaft, wenn man zusehen muss, wie sie sich entwickelt.

Es sieht nicht so aus, als ob der politische Wille vorhanden wäre, die Dinge umzukehren, wenn es um Transparenz geht. Der Gesundheits- und Sozialminister Alex Azar begann [laut Wired](https://www.wired.com/story/trumps-coronavirus-press-event-was-even-worse-than-it-looked/) "über die Tests zu sprechen, mit denen das Gesundheitspersonal feststellt, ob jemand mit dem neuen Coronavirus infiziert ist. Der Mangel an diesen Kits hat zu einem gefährlichen Mangel an epidemiologischen Informationen über die Verbreitung und den Schweregrad der Krankheit in den USA geführt, der durch die Undurchsichtigkeit der Regierung noch verschärft wurde. Azar versuchte zu sagen, dass weitere Tests in Erwartung einer Qualitätskontrolle unterwegs seien. Aber sie machten weiter:

> Dann schnitt Trump Azar den Weg ab. "Aber ich denke, wichtig ist, dass jeder, der jetzt und gestern einen Test braucht, einen Test bekommt. Sie sind da, sie haben die Tests, und die Tests sind schön. Jeder, der einen Test braucht, bekommt einen Test", sagte Trump. Das ist nicht wahr. Vizepräsident Pence sagte den Reportern am Donnerstag, dass die USA nicht genug Testkits hätten, um die Nachfrage zu befriedigen.

Andere Länder reagieren viel schneller und deutlicher als die USA. Viele Länder in Südostasien zeigen großartige Ergebnisse, darunter Taiwan, wo R0 jetzt auf 0,3 gesunken ist, und Singapur, das als Modell für die [COVID-19-Reaktion](https://www.medpagetoday.com/infectiousdisease/covid19/85254) vorgeschlagen wird. Aber nicht nur in Asien; in Frankreich beispielsweise ist jede Versammlung von >1000 Personen verboten, und in drei Distrikten sind die Schulen jetzt geschlossen.

<h2 id='end'>Zum Schluss</h2>

Covid-19 ist ein bedeutendes gesellschaftliches Problem, und wir können und sollten alle daran arbeiten, die Ausbreitung der Krankheit einzudämmen. Das bedeutet:


- Vermeidung großer Gruppen und Menschenmengen
- Absagen von Veranstaltungen.
- Wenn möglich, von zu Hause aus arbeiten
- Händewaschen beim Kommen und Gehen von zu Hause und häufig auch unterwegs
- Vermeiden Sie es, Ihr Gesicht zu berühren, besonders wenn Sie sich außerhalb Ihres Hauses befinden.

<em>Hinweis: Aufgrund der Dringlichkeit, dies herauszubekommen, waren wir nicht so vorsichtig, wie wir es normalerweise gerne wären, wenn wir die Arbeit, auf die wir uns verlassen, zitieren und anerkennen würden. Bitte lassen Sie uns wissen, wenn wir etwas übersehen haben.</em>

Vielen Dank an Sylvain Gugger und Alexis Gallagher für Rückmeldungen und Kommentare.

#### Anmerkung des Übersetzers

<em>Covid-19, Ihre Gemeinschaft und Sie - eine datenwissenschaftliche Perspektive - Übersetzung des Artikels von Jeremy Howard und Rachel Thomas ins Deutsche. Der Originalbeitrag ist <a href="https://www.fast.ai/2020/03/09/coronavirus/#this-is-not-like-the-flu">hier</a>. 
Und wenn jemand Rechtschreib-, Grammatik- oder Tippfehler sieht, und beitragen möchte, Ich habe gerade den <a href="https://github.com/multitudes/covid19/blob/master/Covid19.md">Markdown auf GitHub</a> hochgeladen (Fußnoten funktionieren dort nicht ;)</em>

<br>
</br>

## Fußnoten

(Klicken Sie ↩ auf eine Fußnote, um zu dem Ort zurückzukehren, an dem Sie sich befanden).



<div class="footnotes">
<ol>
<li id="fn:epid"><p>
<em>Epidemiologen</em> sind Menschen, die die Ausbreitung von Krankheiten untersuchen. Es hat sich herausgestellt, dass die Einschätzung von Dingen wie Mortalität und R0 eigentlich ziemlich schwierig ist, so dass es ein ganzes Feld gibt, das sich darauf spezialisiert hat, dies gut zu tun. Wir sind misstrauisch gegenüber Menschen, die einfache Kennzahlen und Statistiken verwenden, um Ihnen zu sagen, wie sich Covid-19 verhält. Schauen Sie sich stattdessen die von Epidemiologen erstellten Modelle an. <a class="reversefootnote" href="#fnref:epid">↩</a></p>
</li>

<li id="fn:r0"><p>
Nun, technisch gesehen ist das nicht wahr. "R0" bezieht sich streng genommen auf die Infektionsrate bei Abwesenheit einer Reaktion. Aber da uns das eigentlich nie wirklich interessiert, lassen wir hier unsere Definitionen ein wenig nachlässig sein.<a class="reversefootnote" href="#fnref:r0">↩</a></p>
</li>

<li id="fn:letdown"><p>
Seit dieser Entscheidung haben wir hart daran gearbeitet, einen Weg zu finden, um den Kurs virtuell durchzuführen, und wir hoffen, dass er noch besser sein wird, als die Version vor Ort gewesen wäre. Wir konnten jetzt den Kurs für jeden auf der Welt anbieten und werden jeden Tag virtuelle Studien- und Projektgruppen durchführen.<a class="reversefootnote" href="#fnref:letdown">↩</a></p>
</li>

<li id="fn:changes"><p>
Wir haben auch viele andere kleinere Änderungen in unserem Lebensstil vorgenommen, darunter zu Hause zu trainieren, anstatt ins Fitnessstudio zu gehen, alle unsere Sitzungen auf Videokonferenz zu verlegen und Abendveranstaltungen auf die wir uns schon immer gefreut hatten, zu überspringen.<a class="reversefootnote" href="#fnref:changes">↩</a></p>
</li>

</ol>
</div>

[12]: https://www.reuters.com/article/us-health-coronavirus-italy/alarmed-italy-locks-down-north-to-prevent-spread-of-coronavirus-idUSKBN20V06R
