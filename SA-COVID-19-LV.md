---
title: Laikrindu sezonālā koriģēšana COVID-19 krīzes laikā
author: Centrālā statistikas pārvalde
date: 2020. gada 28. maijs
---

# Ievads

Laikrindu sezonālās un kalendārās koriģēšanas primārie mērķi ir:

- izslēgt no laikrindas kalendāros efektus (darbdienu vai nedēļas dienu efekts, garā gada efekts);
- izslēgt no laikrindas zināmas un novērojamas sezonālās svārstības, kuras regulāri atkārtojas katru gadu;

Sekundārais mērķis ir:

- novērtēt laikrindas tendenci (jeb *trendu*).

Laikrindu koriģēšanas problemātiku krīzes laikā var sadalīt divās daļās - sezonālā koriģēšana (šeit un turpmāk, ietverot kalendāro koriģēšanu) un tendences novērtēšana.


# Laikrindu sezonālā koriģēšana krīzes laikā

Parasti ar katru jaunu datu punktu (periodu) mēs saņem jaunu informāciju par laikrindu. Attiecīgi ar katru jaunu datu punktu ir iespēja pārrēķināt sezonālos un kalendāros efektus, ņemot vērā jauno informāciju. Pastāv dažādas prakses attiecībā uz sezonālo un kalendāro efektu pārrēķināšanu. CSP sezonālos un kalendāros efektus pārrēķina ar katru papildus datu punktu.

Krīzes laiks ir īpašs ar to, ka mēs nesaņemsim jaunu informāciju par sezonalitāti (tai skaitā par kalendārajiem efektiem). Tas ir tāpēc, ka krīze nav sezonāla. Lielas krīzes (tai skaitā COVID-19 krīze) ir retas parādības, kuras nenotiek katru gadu ar vienu un to pašu periodiskumu[^1].

[^1]: Te gan jāpiebilst, ka izskan hipotēze par to, ka šāda vīrusa epidēmija var kļūt sezonāla. Ja piepildīsies šāds scenārijs, tad vīrusu epidēmijas krīzes efekti tiks koriģēti kā sezonāli efekti. Krīzes laikā nesaņemam aktuālu informāciju par sezonalitāti, attiecīgi laikrindas sezonalitāti varam novērtēt tikai no datiem līdz krīzes sākumam.

Lai tehniski "iesaldētu" sezonalitāti un neveiktu sezonalitātes pārrēķināšanu ar krīzes perioda datiem, var lietot divas metodes:

1. Primārā metode - visi laikrindas punkti krīzes ietekmes periodā tiek definēti kā izlēcēji. Šajā gadījumā izlēcējs krīzes ietekmes punktā tiek pievienots arī tad, ja tā novērtējums ir nenozīmīgs.
1. Sekundārā metode - [laikrindas modeļa fiksēšana](https://jdemetradocumentation.github.io/JDemetra-documentation/pages/case-studies/revision-fixed.html) (vadlīnijās un JDemetra+ to sauc par *Current Adjustment* vai *Fixed Model*). Pielietojot šo metodi, tiek fiksēti izlēcēju un citu regresoru koeficientu novērtējumi. Tie netiek pārrēķināti ar jaunajiem datiem. Procedūra nepievieno jaunus izlēcējus, bet lietotājs tos var pievienot manuāli.

Abos gadījumos mēs sezonālās koriģēšanas algoritmam (programmā [JDemetra+](https://github.com/jdemetra)) "paziņojam", ka laikrindas krīzes ietekmes perioda vērtības nav izmantojamas sezonalitātes pārrēķināšanai.

Izmantotās metodes ir saskaņotas ar Eiropas Statistikas biroja (*Eurostat*) publicētajām krīzes vadlīnijām (*[Guidance on time series treatment in the context of the Covid-19 crisis](https://ec.europa.eu/eurostat/data/metadata/covid-19-support-for-statisticians)*) un ESS Sezonālās koriģēšanas palīdzības dienestu (*[ESS Seasonal Adjustment Helpdesk](https://ec.europa.eu/eurostat/cros/content/ess-seasonal-adjustment-helpdesk_en)*).


# Tendences novērtēšana krīzes laikā

Krīzei uz laikrindas tendenci var būt divējāda ietekme:

- pārejoša ietekme uz tendenci - krīzes laikā ir ietekme, bet pēc krīzes ietekme uzreiz vai pakāpeniski pazūd un laikrindas tendence atgriežas pirms krīzes stāvoklī;
- paliekoša ietekme uz tendenci - krīzes laikā ir ietekme, kura ir paliekoša arī pēc krīzes beigām.

Krīzes laikā (īpaši krīzes sākumā) ar matemātisku metožu palīdzību nav iespējams noteikt, kurš no šiem scenārijiem ir spēkā. Tāpēc ir ļoti svarīgi kā papildus informāciju izmantot ekonomikas ekspertu vērtējumu par krīzes ietekmi uz laikrindas tendenci.

Jāpiebilst, ka tendences novērtēšana laikrindas sākuma vai beigu punktos nav ieteicama. Tendences novērtējumi (īpaši krīzes laikā) var būt neprecīzi un pakļauti lielām revīzijām.


# Kopsavilkums

- COVID-19 krīze laikrindu analīzes jomā šobrīd tiek uzskatīta kā notikums, kas nav sezonāls. Attiecīgi krīzes ietekme netiek izslēgta no datiem, veicot sezonālo koriģēšanu.

- Krīzes laikā jaunu informāciju par sezonālajiem un kalendārajiem efektiem nesaņemam, jo krīzes ietekme neļauj tos novērot. Tāpēc sezonālie un kalendārie efekti tiek novērtēti, izmantojot pirms krīzes perioda datus.

- Krīzes ietekmes perioda datiem tiek veikta sezonālā vai kalendārā korekcija. Sezonālie un kalendārie efekti krīzes ietekmes periodā ir novērtēti, izmantojot pirms krīzes perioda datus.

- Jāņem vērā, ka krīzes laikā gan nekoriģēti, gan sezonāli un kalendāri koriģēti dati var tikt pakļauti lielākām datu revīzijām nekā tas ir parasti.

- Tendences novērtējumi (īpaši krīzes laikā) var būt neprecīzi un pakļauti lielām revīzijām.



# Literatūra

- ESS SA Helpdesk (2019) [A brief description of JDemetra+](https://jdemetradocumentation.github.io/JDemetra-documentation/)
- Eurostat (2015) [ESS guidelines on seasonal adjustment](https://ec.europa.eu/eurostat/web/products-manuals-and-guidelines/-/KS-RA-09-006), section *2.8. Treatment of outliers at the end of the series and at the beginning of a major economic change*
- Eurostat (2020) [Guidance on time series treatment in the context of the Covid-19 crisis](https://ec.europa.eu/eurostat/data/metadata/covid-19-support-for-statisticians)
- Eurostat (2020) [Data collection for the EU-Labour Force Survey in the context of the Covid-19 crisis](https://ec.europa.eu/eurostat/data/metadata/covid-19-support-for-statisticians)
- Statistics Norway (2020) [Seasonal adjustment during the Corona crisis](https://github.com/statisticsnorway/SeasonalAdjustmentCorona)
