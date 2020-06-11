# Laikrindu sezonālā koriģēšana COVID-19 krīzes laikā

**Centrālā statistikas pārvalde**

*2020. gada 9. jūnijs*


## Ievads

Laikrindu sezonālās un kalendārās koriģēšanas primārie mērķi ir:

- izslēgt no laikrindas kalendāros efektus (darbdienu vai nedēļas dienu efekts, garā gada efekts);
- izslēgt no laikrindas zināmas un novērojamas sezonālās svārstības, kuras regulāri atkārtojas katru gadu.

Sekundārais mērķis ir:

- novērtēt laikrindas tendenci (jeb *trendu*).

Laikrindu koriģēšanas problemātiku krīzes laikā var sadalīt divās daļās - sezonālā koriģēšana (šeit un turpmāk, ietverot kalendāro koriģēšanu) un tendences novērtēšana.

Lai arī krīze ietekmē gandrīz visus ekonomiskos un sociālos procesus, tomēr ir laikrindas, kurām  krīzes ietekme nav ekonomiski pamatojama. Šādas laikrindas krīzes laikā tiek koriģētas atbilstoši standarta procedūrām. Turpmākais dokumenta saturs attiecas tikai uz laikrindām, kurām krīzes ietekme ir ekonomiski pamatojama.

Centrālā statistikas pārvalde (CSP) laikrindu sezonālo un kalendāro koriģēšanu veic ar programmu [JDemetra+ 2.2.2](https://github.com/jdemetra/jdemetra-app/releases), izmantojot [TRAMO-SEATS metodi](https://jdemetradocumentation.github.io/JDemetra-documentation/pages/theory/).


## Laikrindu sezonālā koriģēšana krīzes laikā

Parasti ar katru jaunu datu punktu (periodu) mēs saņemam jaunu informāciju par laikrindu. Attiecīgi ar katru jaunu datu punktu ir iespēja pārrēķināt sezonālos un kalendāros efektus, ņemot vērā jauno informāciju. Pastāv dažādas prakses attiecībā uz sezonālo un kalendāro efektu pārrēķināšanu. CSP sezonālos un kalendāros efektus pārrēķina ar katru papildus datu punktu.

Krīzes laiks ir īpašs ar to, ka mēs nesaņemam jaunu informāciju par sezonalitāti (tai skaitā par kalendārajiem efektiem). Tas ir tāpēc, ka krīze nav sezonāla. Lielas krīzes (tai skaitā COVID-19 krīze) ir retas parādības, kuras nenotiek katru gadu ar vienu un to pašu periodiskumu.

*Te gan jāpiebilst, ka izskan hipotēze par to, ka šāda vīrusa epidēmija var kļūt sezonāla. Ja piepildīsies šāds scenārijs, tad vīrusu epidēmijas krīzes efekti tiks koriģēti kā sezonāli efekti.*

Krīzes laikā laikrindu sezonalitāti varam novērtēt tikai no datiem līdz krīzes sākumam. Lai tehniski "iesaldētu" sezonalitāti un neveiktu sezonalitātes pārrēķināšanu ar krīzes perioda datiem, CSP lieto divas metodes:

1. Primārā metode - visi laikrindas punkti, kurus ietekmē krīze, tiek definēti kā izlēcēji. Šajā gadījumā izlēcējs krīzes ietekmes punktā tiek pievienots arī tad, ja tā novērtējums ir nenozīmīgs.
1. Sekundārā metode - [laikrindas modeļa fiksēšana](https://jdemetradocumentation.github.io/JDemetra-documentation/pages/case-studies/revision-fixed.html) (vadlīnijās un [JDemetra+](https://github.com/jdemetra) to sauc par *Current Adjustment* vai *Fixed Model*). Pielietojot šo metodi, tiek fiksēti izlēcēju un citu regresoru koeficientu novērtējumi. Tie netiek pārrēķināti ar jaunajiem datiem. Procedūra nepievieno jaunus izlēcējus, bet lietotājs tos var pievienot manuāli.

Pārsvarā visos gadījumos tiek lietota primārā metode. Gadījumos, kad papildus sezonālajai koriģēšanai ir nepieciešams laikrindas tendences novērtējums, tiek lietota sekundārā metode. Abos gadījumos mēs sezonālās koriģēšanas algoritmam (programmā [JDemetra+](https://github.com/jdemetra)) "paziņojam", ka laikrindas krīzes ietekmes perioda vērtības nav izmantojamas sezonalitātes pārrēķināšanai. Izmantotās metodes ir saskaņotas ar Eiropas Statistikas biroja (*Eurostat*) publicētajām krīzes vadlīnijām (*[Guidance on time series treatment](https://ec.europa.eu/eurostat/documents/10186/10693286/Time_series_treatment_guidance.pdf)*) un ESS Sezonālās koriģēšanas palīdzības dienestu (*[ESS Seasonal Adjustment Helpdesk](https://ec.europa.eu/eurostat/cros/content/ess-seasonal-adjustment-helpdesk_en)*).


## Tendences novērtēšana krīzes laikā

Krīzei uz laikrindas tendenci var būt divējāda ietekme:

- pārejoša ietekme uz tendenci - krīzes laikā ir ietekme, bet pēc krīzes ietekme uzreiz vai pakāpeniski pazūd un laikrindas tendence atgriežas pirms krīzes stāvoklī;
- paliekoša ietekme uz tendenci - krīzes laikā ir ietekme, kura ir paliekoša arī pēc krīzes beigām.

Krīzes laikā (īpaši krīzes sākumā) ar matemātisku metožu palīdzību nav iespējams noteikt, kurš no šiem scenārijiem ir spēkā. Tāpēc ir ļoti svarīgi kā papildus informāciju izmantot ekonomikas ekspertu vērtējumu par krīzes ietekmi uz laikrindas tendenci.

Jāpiebilst, ka tendences novērtēšana laikrindas sākuma vai beigu punktos nav ieteicama. Tendences novērtējumi (īpaši krīzes laikā) var būt neprecīzi un pakļauti lielām revīzijām.


## Kopsavilkums

- COVID-19 krīze laikrindu analīzes jomā šobrīd tiek uzskatīta kā notikums, kas nav sezonāls. Attiecīgi krīzes ietekme netiek izslēgta no datiem, veicot sezonālo koriģēšanu.

- Krīzes laikā jaunu informāciju par sezonālajiem un kalendārajiem efektiem nesaņemam, jo krīzes ietekme neļauj tos novērot. Tāpēc sezonālie un kalendārie efekti tiek novērtēti, izmantojot tikai pirms krīzes perioda datus.

- Krīzes ietekmes perioda datiem tiek veikta sezonālā vai kalendārā korekcija ar sezonālajiem un kalendārajiem efektiem, kas ir novērtēti, izmantojot pirms krīzes perioda datus.

- Jāņem vērā, ka krīzes laikā gan nekoriģēti, gan sezonāli un kalendāri koriģēti dati var tikt pakļauti lielākām datu revīzijām nekā tas ir parasti.

- Tendences novērtējumi (īpaši krīzes laikā) var būt neprecīzi un pakļauti lielām revīzijām.



## Literatūra

- ESS SA Helpdesk (2019) [A brief description of JDemetra+](https://jdemetradocumentation.github.io/JDemetra-documentation/)
- Eurostat (2015) [ESS guidelines on seasonal adjustment](https://ec.europa.eu/eurostat/web/products-manuals-and-guidelines/-/KS-RA-09-006), section *2.8. Treatment of outliers at the end of the series and at the beginning of a major economic change*
- Eurostat (2020) [Guidance on time series treatment](https://ec.europa.eu/eurostat/documents/10186/10693286/Time_series_treatment_guidance.pdf)
- Eurostat (2020) [Guidance on the EU-Labour Force Survey data collection](https://ec.europa.eu/eurostat/documents/10186/10693286/LFS_guidance.pdf)
- Statistics Norway (2020) [Seasonal adjustment during the Corona crisis](https://github.com/statisticsnorway/SeasonalAdjustmentCorona)
