# Proyecto PAX

## Análisis de la aplicación de un pipeline bioinformático de RNAseq en pacientes con poliposis adenomatosa tipo X sin diagnóstico molecular.

El cáncer colorrectal (CCR) es uno de los tipos de cáncer más frecuentes y de mayor mortalidad a nivel
mundial, presentando una incidencia del 10.2% y acabando anualmente con la vida de en torno al 9% de
la población (teniendo una mayor prevalencia general en el sexo masculino) 1,2
Aunque la mayoría de los casos de CCR son esporádicos, se estima que en torno al 5% del total es debido
los llamados Síndromes de Cáncer Hereditario3,4, donde los pacientes son portadores de variantes
patogénicas en la línea germinal en ciertos genes de susceptibilidad al cáncer, presentando un mayor
riesgo en la aparición de tumores3. Según el modelo clásico de carcinogénesis colorrectal los
adenocarcinomas colorrectales malignos son precedidos por pólipos adenomatosos colónicos 5,6, por lo
que un diagnóstico precoz de los mismos permite un seguimiento más rutinario de los pacientes ayudando
a la prevención en la aparición de CCR.

La poliposis adenomatosa familiar (PAF) es una entidad clínica caracterizada por la aparición de múltiples
pólipos adenomatosos distribuidos a lo largo de todo el colon y un mayor riesgo de desarrollo de cáncer
colorrectal. La presentación clínica es variable, distinguiéndose poliposis adenomatosa familiar (FAP - gen
APC; OMIM#175100) y poliposis asociada a la corrección de lectura de la polimerasa (PPAP - genes
POLE/POLD1; OMIM#612591/615083) con un patrón de herencia autosómico dominante, poliposis
asociada a MUTYH (MAP; OMIM#608456) y poliposis asociada a NTHL1 (NAP; OMIM#616415 con un
patrón de herencia autosómico recesivo. Sin embargo, las variantes encontradas en estos genes conceden
un rendimiento diagnóstico de en torno al 10% de los casos7, quedando el 90% restante sin una
explicación genética asociada. El abordaje clínico y el pronóstico de los individuos con poliposis
adenomatosa y sus familiares es dependiente de su etiología genética, por lo que su diagnóstico y el
establecimiento de relaciones genotipo-fenotipo resulta de gran interés.
Debido a esta situación, en los últimos años se han estudiado genes de menor incidencia en el desarrollo
de la poliposis adenomatosa (AXIN2, BMPR1A, MLH1, MLH3, MSH2, MSH3, PTEN, NTHL1, PMS2, PMS2CL,
POLD1, POLE, SMAD4, STK11, GALNT12)8–12 y se han planteado técnicas de análisis de alteraciones no
codificantes como la secuenciación del transcriptoma (RNAseq)13 que podrían ayudar a completar un
porcentaje de los casos con poliposis adenomatosa familiar sin diagnóstico genético conocido, también
definidos como pacientes con poliposis adenomatosa tipo X (PAX).
Hoy en día, la llegada de la secuenciación de nueva generación (NGS) o secuenciación masiva ha permitido
el desarrollo de paneles que permiten la secuenciación de genes de interés y presentan la ventaja de tener
un diseño muy optimizado y una gran cobertura y profundidad de lectura8. De la misma forma, el RNAseq
nos permite una visión directa de las perturbaciones transcripcionales causadas por los cambios genéticos
y se ha utilizado previamente para observar el efecto de variantes patógenas, que se identificaron
mediante NGS14,15. Sin embargo, a pesar de que los estudios piloto que utilizan RNAseq para la
investigación de variantes causantes de enfermedades genéticas raras han obtenido un aumento de las
tasas de diagnóstico de un 8-36% más que aquellos en los que solo se evaluaron mediante tecnología
NGS16, actualmente no se aplican de forma sistemática al diagnóstico clínico de enfermedades
hereditarias17.

En este trabajo de fin de máster (TFM) describimos la aplicación de varias herramientas bioinformáticas
para evaluar el rendimiento diagnóstico del estudio del transcriptoma de pacientes que no han podido
obtener un resultado genético compatible con su patología mediante técnicas convencionales NGS; en
nuestro caso un panel NGS de genes PAX (Panel PAX: APC, MUTYH, AXIN2, BMPR1A, MLH1, MLH3, MSH2, MSH3, PTEN, NTHL1, PMS2, PMS2CL, POLD1, POLE, SMAD4, STK11, GALNT12).
Entre las aproximaciones a estudiar se encuentra la herramienta STAR-Fusion, DROP - pipeline (del inglés Detection of RNA Outliers Pipeline)16 y además, abordaremos un paso más en el intento de obtener alguna confirmación de diagnóstico extra con la comparación de algunas herramientas utilizadas en el estudio de inversiones en RNA.
El interés de este estudio reside en su utilidad clínica y traslacional, ya que una vez evaluado se pretende implementar dicho pipeline (STAR-Fusion + DROP-pipeline + herramienta de detección de fusiones) de análisis RNAseq en nuestro centro de trabajo para su uso en proyectos de investigación y/o incorporación a la rutina asistencial en el futuro. De esta forma, si se consiguieran unos resultados relevantes clínicamente supondría un paso hacia la instauración de este tipo de tecnologías en la rutina diagnóstica, ayudando al establecimiento de guías clínicas más ajustadas y a un mejor asesoramiento y manejo clínico de estos pacientes.

## Bibliografía

1. Goodarzi, E., Sohrabivafa, M., Dehkordi, A. & Khazaei, Z. Worldwide incidence and mortality of bladder cancer and human development index: An ecological study. Indian J. Med. Spec. 11, 88 (2020).
2. Kim, S. E. et al. Sex- and gender-specific disparities in colorectal cancer risk. World J. Gastroenterol. 21, 5167–5175 (2015).
3. Foulkes, W. D. Inherited Susceptibility to Common Cancers. N. Engl. J. Med. 359, 2143–2153 (2008).
4. Peters, U., Bien, S. & Zubair, N. Genetic architecture of colorectal cancer. Gut 64, 1623–1636 (2015).
5. Fearon, E. R. & Vogelstein, B. A genetic model for colorectal tumorigenesis. Cell 61, 759–767 (1990).
6. Gehart, H. & Clevers, H. Tales from the crypt: new insights into intestinal stem cells. Nat. Rev. Gastroenterol. Hepatol. 2018 161 16, 19–34 (2018).
7. Grover, S. et al. Prevalence and Phenotypes of APC and MUTYH Mutations in Patients with Multiple Colorectal Adenomas. JAMA 308, 485 (2012).
8. Valle, L. et al. Update on genetic predisposition to colorectal cancer and polyposis. Mol. Aspects Med. 69, 10–26 (2019).
9. Lorca, V. et al. Role of GALNT12 in the genetic predisposition to attenuated adenomatous polyposis syndrome. PLoS One 12, (2017).
10. Evans, D. R. et al. Evidence for GALNT12 as a moderate penetrance gene for colorectal cancer. Hum. Mutat. 39, 1092–1101 (2018).
11. Te Paske, I. B. A. W., Ligtenberg, M. J. L., Hoogerbrugge, N. & de Voer, R. M. Candidate gene discovery in hereditary colorectal cancer and polyposis syndromes—considerations for future studies. Int. J. Mol. Sci. 21, 1–21 (2020).
12. Tsoulos, N. et al. Analysis of hereditary cancer syndromes by using a panel of genes: Novel and multiple pathogenic mutations. Cancer Res. 79, P4-03-07-P4-03–07 (2019).
13. Cummings, B. B. et al. Improving genetic diagnosis in Mendelian disease with transcriptome sequencing. Sci. Transl. Med. 9, (2017).
14. Gonorazky, H. et al. RNAseq analysis for the diagnosis of muscular dystrophy. Ann. Clin. Transl. Neurol. 3, 55–60 (2015).
15. Wang, K. et al. Whole-genome DNA/RNA sequencing identifies truncating mutations in RBCK1 in a novel Mendelian disease with neuromuscular and cardiac involvement. Genome Med. 5, (2013).
16. Yépez, V. A. et al. Detection of aberrant gene expression events in RNA sequencing data. Nat. Protoc. 16, 1276–1296 (2021).
17. Cummings, B. B. et al. Genotype-Tissue Expression Consortium. Sci Transl Med 12, 1–25 (2017).
