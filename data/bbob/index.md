---
layout: default
title: The BBOB Example
permalink: /data/bbob/
---
# The BBOB Example

In this folder, we provide an example data set of testing the application of the {{ site.projectNameStyled }} evaluator. We use it to investigate some of the results of the [Black-Box Optimization Benchmarking (BBOB) 2013](http://coco.gforge.inria.fr/doku.php?id=bbob-2013) .

## 1. Example Structure

This example is structured as follows

1. The archive [`results.zip`](results.zip) contains the results of these algorithms. These results are stored in the format native to COCO without any modification except that we left away files that our system does not need to make the example smaller.
2. The file [`evaluation.xml`](evaluation.xml) contains an example evaluation definition. We apply a set of different modules and configurations.
3. The file [`configForIEEEEtran.xml`](configForIEEEEtran.xml) is a configuration that applies [`evaluation.xml`](evaluation.xml) to the [results](results.zip) and renders the output as LaTeX document styled according to `IEEEtran.cls` into a folder named `reports/LaTeX/IEEEtran/`. 
6. The file [`configForLNCS.xml`](configForLNCS.xml) is a configuration that applies [`evaluation.xml`](evaluation.xml) to the [results](results.zip) and renders the output as LaTeX document styled according to `LLNCS.cls` into a folder named `reports/LaTeX/LNCS/`.
6. The file [`configForSigAlternate.xml`](configForSigAlternate.xml) is a configuration that applies [`evaluation.xml`](evaluation.xml) to the [results](results.zip) and renders the output as LaTeX document styled according to `sig-alternate.cls` into a folder named `reports/LaTeX/SigAlternate/`.
6. The file [`configForXHTML.xml`](configForXHTML.xml) is a configuration that applies [`evaluation.xml`](evaluation.xml) to the [results](results.zip) and renders the output as XHTML document into a folder named `reports/XHTML/`.
6. The file [`configForExport.xml`](configForExport.xml) is a configuration that applies [`evaluation.xml`](evaluation.xml) to the [results](results.zip) and renders the output as text (for import into other tools) into a folder named `reports/export/`.

## 2. BBOB and COCO

COmparing Continuous Optimisers ([COCO](http://coco.gforge.inria.fr/doku.php?id=start)) is a platform for systematic and sound comparisons of real-parameter global optimization algorithms. COCO provides benchmark functions, experimentation templates which are easy to parallelize, and tools for processing and visualizing data generated by one or several optimization algorithms. The COCO platform has been used for the Black-Box-Optimization-Benchmarking (BBOB) workshops that took place during several GECCO conference since 2009.

The example data used here was gathered by other researchers following the COCO [experimental procedure](http://coco.lri.fr/BBOB-downloads/download10.0/bbobdocexperiment.pdf) on the [noiseless benchmark functions](http://coco.lri.fr/downloads/download13.09/bbobdocfunctions.pdf).

## 3. Experimental Data

The algorithms are described [here](http://coco.gforge.inria.fr/doku.php?id=bbob-2013-algorithms) and were investigated independently by their respective authors. We do not claim, own, or assume any responsibility, copyright, authorship, or liability for any of the data provided here.

<table>
<tr><th style="text-align:left;vertical-align:top">1.&nbsp;<a href="http://coco.gforge.inria.fr/data-archive/2013/GA-100_holtschulte_noiseless.tgz"><code>holtschulte2013_ga100</code></a></th>
<td  style="text-align:left;vertical-align:top">
Neal Holtschulte and Melanie Moses.
<a href="http://coco.gforge.inria.fr/lib/exe/fetch.php?media=pdf2013:w0309-holtschulte.pdf">Benchmarking Cellular Genetic Algorithms on the BBOB Noiseless Testbed</a>. GECCO'13 Companion, July 6–10, 2013, Amsterdam, The Netherlands. ACM 978-1-4503-1964-5/13/07</td>
</tr>

<tr><th style="text-align:left;vertical-align:top">2.&nbsp;<a href="http://coco.gforge.inria.fr/data-archive/2013/HILL_holtschulte_noiseless.tgz"><code>holtschulte2013_hill</code></a></th>
<td  style="text-align:left;vertical-align:top">
Neal Holtschulte and Melanie Moses.
<a href="http://coco.gforge.inria.fr/lib/exe/fetch.php?media=pdf2013:w0309-holtschulte.pdf">Benchmarking Cellular Genetic Algorithms on the BBOB Noiseless Testbed</a>. GECCO'13 Companion, July 6–10, 2013, Amsterdam, The Netherlands. ACM 978-1-4503-1964-5/13/07</td>
</tr>

<tr><th style="text-align:left;vertical-align:top">3.&nbsp;<a href="http://coco.gforge.inria.fr/data-archive/2013/CMAES_Hutter_hutter_noiseless.tgz"><code>hutter2013_CMAES</code></a></th>
<td  style="text-align:left;vertical-align:top">
Frank Hutter, Holger Hoos, and Kevin Leyton-Brown.
<a href="http://coco.gforge.inria.fr/lib/exe/fetch.php?media=pdf2013:w0311-hutter.pdf">An Evaluation of Sequential Model-Based Optimization for Expensive Blackbox Functions</a>. GECCO'13 Companion, July 6–10, 2013, Amsterdam, The Netherlands. ACM 978-1-4503-1964-5/13/07</td>
</tr>

<tr><th style="text-align:left;vertical-align:top">4.&nbsp;<a href="http://coco.gforge.inria.fr/data-archive/2013/IP_liao_noiseless.tgz"><code>liao2013_IPOP</code></a></th>
<td  style="text-align:left;vertical-align:top">
Tianjun Liao and Thomas Stützle.
<a href="http://coco.gforge.inria.fr/lib/exe/fetch.php?media=pdf2013:w0305-liao.pdf">Testing the Impact of Parameter Tuning on a Variant of IPOP-CMA-ES with a Bounded Maximum Population Size on the Noiseless BBOB Testbed</a>. GECCO'13 Companion, July 6–10, 2013, Amsterdam, The Netherlands. ACM 978-1-4503-1964-5/13/07</td>
</tr>

<tr><th style="text-align:left;vertical-align:top">5.&nbsp;<a href="http://coco.gforge.inria.fr/data-archive/2013/texp_liao_noiseless.tgz"><code>liao2013_IPOP-texp</code></a></th>
<td  style="text-align:left;vertical-align:top">
Tianjun Liao and Thomas Stützle.
<a href="http://coco.gforge.inria.fr/lib/exe/fetch.php?media=pdf2013:w0305-liao.pdf">Testing the Impact of Parameter Tuning on a Variant of IPOP-CMA-ES with a Bounded Maximum Population Size on the Noiseless BBOB Testbed</a>. GECCO'13 Companion, July 6–10, 2013, Amsterdam, The Netherlands. ACM 978-1-4503-1964-5/13/07</td>
</tr>

<tr><th style="text-align:left;vertical-align:top">6.&nbsp;<a href="http://coco.gforge.inria.fr/data-archive/2013/DE_Pal_pal_noiseless.tgz"><code>pal2013_DE</code></a></th>
<td  style="text-align:left;vertical-align:top">
László Pál.
<a href="http://coco.gforge.inria.fr/lib/exe/fetch.php?media=pdf2013:w0302-pal.pdf">Benchmarking a Hybrid Multi Level Single Linkage Algorithm on the BBOB Noiseless Testbed</a>. GECCO'13 Companion, July 6–10, 2013, Amsterdam, The Netherlands. ACM 978-1-4503-1964-5/13/07</td>
</tr>

<tr><th style="text-align:left;vertical-align:top">7.&nbsp;<a href="http://coco.gforge.inria.fr/data-archive/2013/fmincon_pal_noiseless.tgz"><code>pal2013_fmincon</code></a></th>
<td  style="text-align:left;vertical-align:top">
László Pál.
<a href="http://coco.gforge.inria.fr/lib/exe/fetch.php?media=pdf2013:w0303-pal.pdf">Comparison of Multistart Global Optimization Algorithms on the BBOB Noiseless Testbed</a>. GECCO'13 Companion, July 6–10, 2013, Amsterdam, The Netherlands. ACM 978-1-4503-1964-5/13/07</td>
</tr>

<tr><th style="text-align:left;vertical-align:top">8.&nbsp;<a href="http://coco.gforge.inria.fr/data-archive/2013/HMLSL_pal_noiseless.tgz"><code>pal2013_HMLSL</code></a></th>
<td  style="text-align:left;vertical-align:top">
László Pál.
<a href="http://coco.gforge.inria.fr/lib/exe/fetch.php?media=pdf2013:w0302-pal.pdf">Benchmarking a Hybrid Multi Level Single Linkage Algorithm on the BBOB Noiseless Testbed</a>. GECCO'13 Companion, July 6–10, 2013, Amsterdam, The Netherlands. ACM 978-1-4503-1964-5/13/07</td>
</tr>

<tr><th style="text-align:left;vertical-align:top">9.&nbsp;<a href="http://coco.gforge.inria.fr/data-archive/2013/simplex_pal_noiseless.tgz"><code>pal2013_simplex</code></a></th>
<td  style="text-align:left;vertical-align:top">
László Pál.
<a href="http://coco.gforge.inria.fr/lib/exe/fetch.php?media=pdf2013:w0303-pal.pdf">Comparison of Multistart Global Optimization Algorithms on the BBOB Noiseless Testbed</a>. GECCO'13 Companion, July 6–10, 2013, Amsterdam, The Netherlands. ACM 978-1-4503-1964-5/13/07</td>
</tr>

<tr><th style="text-align:left;vertical-align:top">10.&nbsp;<a href="http://coco.gforge.inria.fr/data-archive/2013/P-DCN_tran_noiseless.tgz"><code>P-DCN</code></a></th>
<td  style="text-align:left;vertical-align:top">
Thanh-Do Tran, Dimo Brockhoff, and Bilel Derbel.
<a href="http://coco.gforge.inria.fr/lib/exe/fetch.php?media=pdf2013:w0312-tran.pdf">Multiobjectivization with NSGA-II on the Noiseless BBOB Testbed</a>. GECCO'13 Companion, July 6–10, 2013, Amsterdam, The Netherlands. ACM 978-1-4503-1964-5/13/07</td>
</tr>

</table>
 

## 4. License

The copyright of the datasets belong to their respective owners. The file [`results.zip`](results.zip) is thus excempt from this project's general licensing terms.

## References
1. Nikolaus Hansen, Anne Auger, Steffen Finck, and Raymond Ros. *Real-parameter black-box optimization benchmarking: Experimental setup*. Technical report, Orsay, France: Université Paris Sud, Institut National de Recherche en Informatiqué et en Automatique INRIA) Futurs, Equipe TAO, March 24, 2012. [URL](http://coco.lri.fr/BBOB-downloads/download11.05/bbobdocexperiment.pdf).
2. Nikolaus Hansen, Anne Auger, Steffen Finck, and Raymond Ros. *Real-parameter black-box optimization benchmarking 2009: Experimental setup*. Rapports de Recherche RR-6828, Institut National de Recherche en Informatique et en Automatique (INRIA), October 16, 2009. [URL](http://hal.archives-ouvertes.fr/inria-00362649/en/). Version 3.
3. Steffen Finck, Nikolaus Hansen, Raymond Ros, and Anne Auger. *Real-parameter black-box optimization benchmarking 2010: Presentation of the noiseless functions*. Technical report, April 13, 2013. [URL](http://coco.lri.fr/downloads/download13.09/bbobdocfunctions.pdf). Working Paper 2009/20, compiled April 13, 2013.