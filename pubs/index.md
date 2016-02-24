---
layout: page
title: Publications
navid: Portfolio
---
<script language="javascript">
      function toggle_abs() {
        var spans = document.getElementsByClassName("abstract");
        var display = "";
        if (document.getElementById("abs").checked) {
          display = "inline";
        } else {
          display = "none";
        }
        for (var i = 0; i < spans.length; i++) {
          spans[i].style["display"] = display;
        }
      }

      function hide_noscript() {
        var to_hide = document.getElementsByClassName("hidejs");
        var to_show = document.getElementsByClassName("showjs");
        for (var i = 0; i < to_hide.length; i++) {
          to_hide[i].style["display"] = "none";
        }
        for (var i = 0; i < to_show.length; i++) {
          to_show[i].style["display"] = "block";
        }
      }
</script>
<p class="showjs">
  <label>
  <input type="checkbox" id="abs" name="abs" onclick="toggle_abs();"/>
  Display publication abstracts.
  </label>
</p>
<p class="hidejs">
  <strong>Please enable javascript to view publication abstracts.</strong>
</p>

<ul class="pubs">
      <li class="epi"><a
        href="http://dx.doi.org/10.1111/irv.12376">Forecasting influenza
        outbreak dynamics in Melbourne from Internet search query surveillance
        data</a><br/>
        <span class="author">
           Moss R, Zarebski A, Dawson P, McCaw JM
        </span><br/>
        <span class="journal">
          <b>Influenza Other Respir Viruses</b>, accepted Jan 2016
        </span><br/>
        <span class="abstract">
        <strong>Background:</strong>
        Accurate forecasting of seasonal influenza epidemics is of great
        concern to healthcare providers in temperate climates, since these
        epidemics vary substantially in their size, timing and duration from
        year to year, making it a challenge to deliver timely and
        proportionate responses.
        Previous studies have shown that Bayesian estimation techniques can
        accurately predict when an influenza epidemic will peak many weeks in
        advance, using existing surveillance data, but these methods must be
        tailored both to the target population and to the surveillance system.
        <br/><strong>Objectives:</strong>
        Our aim was to evaluate whether forecasts of similar accuracy could be
        obtained for metropolitan Melbourne (Australia).
        <br/><strong>Methods:</strong>
        We used the bootstrap particle filter and a mechanistic infection
        model to generate epidemic forecasts for metropolitan Melbourne
        (Australia) from weekly internet search query surveillance data
        reported by Google Flu Trends for 2006–14.
        <br/><strong>Results and Conclusions:</strong>
        Optimal observation models were selected from hundreds of candidates
        using a novel approach that treats forecasts akin to receiver
        operating characteristic (ROC) curves.
        We show that the timing of the epidemic peak can be accurately
        predicted 4–6 weeks in advance, but that the magnitude of the epidemic
        peak and the overall burden are much harder to predict.
        We then discuss how the infection and observation models and the
        filtering process may be refined to improve forecast robustness,
        thereby improving the utility of these methods for healthcare decision
        support.
        </span>
      </li>
      <li class="epi"><a
        href="http://dx.doi.org/10.1371/journal.pcbi.1004334">Innate immunity
        and the inter-exposure interval determine the dynamics of secondary
        influenza virus infection and explain observed viral
        hierarchies</a><br/>
        <span class="author">
           Pengxing Cao, Ada W. C. Yan, Jane M. Heffernan, Stephen Petrie,
           Robert G. Moss, Louise A. Carolan, Teagan A. Guarnaccia,
           Anne Kelso, Ian G. Barr, Jodie McVernon, Karen L. Laurie,
           James M. McCaw
        </span><br/>
        <span class="journal">
          <b>PLOS Comp Biol</b> 11(8): e1004334, Aug 2015
        </span><br/>
        <span class="abstract">
Influenza is an infectious disease that primarily attacks the respiratory
system.
Innate immunity provides both a very early defense to influenza virus invasion
and an effective control of viral growth.
Previous modelling studies of virus–innate immune response interactions have
focused on infection with a single virus and, while improving our
understanding of viral and immune dynamics, have been unable to effectively
evaluate the relative feasibility of different hypothesised mechanisms of
antiviral immunity.
In recent experiments, we have applied consecutive exposures to different
virus strains in a ferret model, and demonstrated that viruses differed in
their ability to induce a state of temporary immunity or viral interference
capable of modifying the infection kinetics of the subsequent exposure.
These results imply that virus-induced early immune responses may be
responsible for the observed viral hierarchy.
Here we introduce and analyse a family of within-host models of re-infection
viral kinetics which allow for different viruses to stimulate the innate
immune response to different degrees.
The proposed models differ in their hypothesised mechanisms of action of the
non-specific innate immune response.
We compare these alternative models in terms of their abilities to reproduce
the re-exposure data.
Our results show that 1) a model with viral control mediated solely by a
virus-resistant state, as commonly considered in the literature, is not able
to reproduce the observed viral hierarchy; 2) the synchronised and
desynchronised behaviour of consecutive virus infections is highly dependent
upon the interval between primary virus and challenge virus exposures and is
consistent with virus-dependent stimulation of the innate immune response.
Our study provides the first mechanistic explanation for the recently observed
influenza viral hierarchies and demonstrates the importance of understanding
the host response to multi-strain viral infections.
Re-exposure experiments provide a new paradigm in which to study the immune
response to influenza and its role in viral control.
        </span>
      </li>
      <li class="renal"><a
        href="http://dx.doi.org/10.1152/ajprenal.00500.2013">Dominant factors
        that govern pressure natriuresis in diuresis and antidiuresis: a
        mathematical model</a><br/>
        <span class="author">
          Moss R, Layton AT
        </span><br/>
        <span class="journal">
          <b>AJP Renal</b> 306(9): F952&ndash;F969, May 2014
        </span><br/>
        <span class="abstract">
  We have developed a whole-kidney model of the urine concentrating mechanism
  and renal autoregulation.
  The model represents the tubuloglomerular feedback (TGF) and myogenic
  mechanisms, which together affect the resistance of the afferent arteriole
  and thus glomerular filtration rate.
  TGF is activated by fluctuations in macula densa [Cl-] and myogenic
  mechanism by changes in hydrostatic pressure.
  The model was used to investigate the relative contributions of medullary
  blood flow autoregulation and inhibition of transport in the proximal
  convoluted tubule to pressure natriuresis in both diuresis and antidiuresis.
  The model predicts that medullary blood flow autoregulation, which only
  affects the interstitial solute composition in the model, has negligible
  influence on the rate of NaCl excretion.
  However, it exerts a significant effect on urine flow, particularly in the
  antidiuretic kidney.
  This suggests that interstitial washout has significant implications for the
  maintenance of hydration status but little direct bearing on salt excretion,
  and that medullary blood flow may only play a signalling role for
  stimulating a pressure-natriuresis response.
  Inhibited reabsorption in the model proximal convoluted tubule is capable of
  driving pressure natriuresis when the known actions of vasopressin on the
  collecting duct epithelium are taken into account.
        </span>
      </li>
      <li class="renal"><a
        href="http://dx.doi.org/10.1152/ajprenal.00089.2013">Hormonal
          regulation of salt and water excretion: a mathematical model of
          whole-kidney function and pressure-natriuresis</a><br/>
        <span class="author">
          Moss R, Thomas SR
        </span><br/>
        <span class="journal">
          <b>AJP Renal</b> 306(2): F224&ndash;F248, Jan 2014
        </span><br/>
        <span class="abstract">
  We present a lumped-nephron model that explicitly represents the main
  features of the underlying physiology, incorporating the major hormonal
  regulatory effects on both tubular and vascular function, and which
  accurately simulates hormonal regulation of renal salt and water excretion.
  This is the first model to explicitly couple glomerulovascular and medullary
  dynamics, and it is much more detailed in structure than existing
  whole-organ models and renal portions of multi-organ models.
  In contrast to previous medullary models, which have only considered the
  antidiuretic state, our model is able to regulate water and sodium excretion
  over a variety of experimental conditions in good agreement with data from
  experimental studies of the rat.
  Since the properties of the vasculature and epithelia are explicitly
  represented, they can be altered to simulate pathophysiological conditions
  and pharmacological interventions.
  The model serves as an appropriate starting point for simulations of
  physiological, pathophysiological and pharmacological renal conditions, and
  for exploring the relationship between the extra-renal environment and renal
  excretory function in physiological and pathophysiological contexts.
        </span>
      </li>
      <li class="epi"><a
        href="http://dx.doi.org/10.1016/j.epidem.2012.12.002">Drivers and
          consequences of influenza antiviral resistant-strain emergence in a
          capacity-constrained pandemic response</a><br/>
        <span class="author">
          Dafilis MP, Moss R, McVernon J, McCaw J
        </span><br/>
        <span class="journal">
          <b>Epidemics</b> 4(4): 219&ndash;226, Dec 2012.
        </span><br/>
        <span class="abstract">
  Antiviral agents remain a key component of most pandemic influenza
  preparedness plans, but concerns exist regarding the likelihood of
  wide-scale distribution to select for drug-resistant variants.
  We used a model that considers the influence of logistical constraints on
  diagnosis and drug delivery to consider achievable "reach" of alternative
  antiviral intervention strategies targeted at cases of varying severity, with
  or without pre-exposure prophylaxis of contacts.
  Within our framework, "real world" constraints substantially reduced
  achievable drug coverage below stated targets as the epidemic progressed.
  Definitive containment of transmission was unlikely but, where observed,
  achieved through early liberal post-exposure prophylaxis of known contacts of
  treated cases.
  Predictors of resistant strain dominance were high intrinsic fitness relative
  to the wild type virus, and early emergence in the course of the epidemic into
  a largely susceptible population, even when drug use was restricted to severe
  case treatment.
        </span>
      </li>
      <li class="renal"><a
        href="http://dx.doi.org/10.1371/journal.pcbi.1002571">Virtual patients
          and sensitivity analysis of the Guyton model of blood pressure
          regulation: towards individualized models of whole-body
          physiology</a><br/>
        <span class="author">
          Moss R, Grosse T, Marchant I, Lassau N, Gueyffier F, Thomas SR
        </span><br/>
        <span class="journal">
          <b>PLOS Comp Biol</b> 8(6): e1002571, Jun 2012.
        </span><br/>
        <span class="abstract">
  We present a methodology for systematically analysing the interactions
  between parameters and outputs in large-scale mathematical models,
  using the Guyton model of circulatory regulation as a case study. This
  model remains a landmark achievement that contributed to the
  development of our current understanding of blood pressure control,
  and we present the first comprehensive sensitivity analysis of this
  model. The results provide new insight into the multi-level
  interactions in the cardiovascular-renal system and will be useful to
  researchers wishing to use the model in pathophysiological or
  pharmacological settings. This methodology is applicable to current
  and future physiological models of arbitrary complexity.
        </span>
      </li>
      <li class="epi"><a
href="http://www.who.int/bulletin/volumes/90/4/11-093419/en/index.html">Likely
          effectiveness of pharmaceutical and non-pharmaceutical interventions
          for mitigating influenza virus transmission in Mongolia</a><br/>
        <span class="author">
          Bolton KJ, McCaw JM, Moss R, Morris RS, Wang S, Burma A, Darma B,
          Narangerel D, Nymadawa P, McVernon J
        </span><br/>
        <span class="journal">
          <b>Bull WHO</b> 90(4): 264&ndash;271, Apr 2012.
        </span><br/>
        <span class="abstract">
  The efficient use of resources to mitigate the spread of an emerging
  infectious disease is of global interest. However, the most
  appropriate control strategies in any given area probably depend on
  the nature of the local population and environment. Implementing
  interventions against emerging infectious diseases is particularly
  important in developing countries, such as Mongolia, where the
  capacity to provide health care and undertake detailed surveillance is
  limited. Here we use the epidemiological data collected during the
  2009 influenza pandemic in Mongolia to calibrate a computational model
  of influenza virus dissemination in a Mongolian pandemic, with
  tailoring to the country’s infrastructural and sociobehavioural
  characteristics. There have been few recent, country-specific
  evaluations of strategies for the mitigation of influenza,
  particularly in resource-poor settings. Our results provide novel
  insights into the probable benefits of anti-influenza interventions in
  Mongolia, some of which are potentially relevant in pandemic planning
  in other low-income regions.
        </span>
      </li>
      <li class="renal"><a
        href="http://dx.doi.org/10.1016/j.pbiomolbio.2011.06.008">Integration
          of detailed modules in a core model of body fluid homeostasis and
          blood pressure regulation</a><br/>
        <span class="author">
          Alfredo I. Hernández, Virginie Le Rolle, David Ojeda, Pierre
          Baconnier, Julie Fontecave-Jallon, François Guillaud, Thibault
          Grosse, Robert G. Moss, Patrick Hannaert, S. Randall Thomas
        </span><br/>
        <span class="journal">
          <b>Prog Biophys Mol Biol</b>, 107(1):169&ndash;182, Oct 2011.
        </span><br/>
        <span class="abstract">
  This paper presents a contribution to the definition of the interfaces
  required to perform heterogeneous model integration in the context of
  integrative physiology. A formalisation of the model integration problem
  is proposed and a coupling method is presented. The extension of the classic
  Guyton model, a multi-organ, integrated systems model of blood pressure
  regulation, is used as an example of the application of the proposed method.
  To this end, the Guyton model has been restructured, extensive sensitivity
  analyses have been performed, and appropriate transformations have been
  applied to replace a subset of its constituting modules by integrating a
  pulsatile heart and an updated representation of the renin-angiotensin
  system. Simulation results of the extended integrated model are presented
  and the impacts of their integration within the original model are evaluated.
        </span>
      </li>
      <li class="epi"><a
        href="http://dx.doi.org/10.1111/j.1750-2659.2011.00209.x">A decision
          support tool for evaluating the impact of a diagnostic-capacity and
          antiviral-delivery constrained intervention strategy on an influenza
          pandemic</a><br/>
        <span class="author">
          James McCaw, Robert Moss, Jodie McVernon
        </span><br/>
        <span class="journal">
          <b>Influenza Other Respi Viruses</b> 5(Suppl. 1): 212&ndash;215, May
          2011.<br/>
          <b>Proceedings:</b> Options for the Control of Influenza VII,
          3&ndash;7 Sep 2010.
        </span><br/>
        <span class="abstract">
  We summarise results from a recently developed model that includes real-world
  constraints, such as finite diagnostic and antiviral distribution capacities.
  We find that use of antiviral agents might be capable of containing or
  substantially mitigating an epidemic in only a small proportion of epidemic
  scenarios given Australia’s existing public health capacities. We then
  introduce a statistical model that, based on just three characteristics of a
  hypothetical outbreak [(i) the basic reproduction number, (ii) the reduction
  in infectiousness of cases when provided with antiviral agents as treatment,
  and (iii) the proportion of cases that present for medical attention],
  accurately predicts whether or not an antiviral intervention strategy will be
  successful. The model highlights the importance of having data collection
  tools in place prior to a pandemic outbreak, so as to make accurate and
  timely estimates of key epidemiological parameters unique (in both time and
  place) to any particular epidemic.
        </span>
      </li>
      <li class="epi"><a
        href="http://dx.doi.org/10.1371/journal.pone.0014505">Diagnosis and
          antiviral intervention strategies for mitigating an influenza
          pandemic</a><br/>
        <span class="author">
          Robert Moss, James McCaw, Jodie McVernon
        </span><br/>
        <span class="journal">
          <b>PLOS ONE</b> 6(2): e14505, Feb 2011.
        </span><br/>
        <span class="abstract">
  We address specific real-world issues that must be considered in order to
  improve pandemic preparedness policy in a practical and methodologically
  sound way. Provision of antivirals on the scale proposed for an effective
  response is infeasible using traditional public health outbreak management
  and contact tracing approaches. The results indicate to change the
  transmission dynamics of an influenza epidemic with an antiviral
  intervention, a decentralised system is required for contact identification
  and prophylaxis delivery, utilising a range of existing services and
  infrastructure in a "whole of society" response.
        </span>
      </li>
      <li class="renal"><a
        href="http://dx.doi.org/10.1016/j.physd.2009.08.015">Discrete network
          models of interacting nephrons</a><br/>
        <span class="author">
          Robert Moss, Ed Kazmierczak, Michael Kirley, Peter Harris
        </span><br/>
        <span class="journal">
          <b>Physica D</b>, 238(22): 2166&ndash;2176, Nov 2009.
        </span><br/>
        <span class="abstract">
  Multi-nephron systems incorporate two competing coupling
  mechanisms&mdash;vascular and hemodynamic&mdash;that enforce in-phase
  and anti-phase synchronisations respectively. Using a two-nephron
  model, we show that the strength of the hemodynamic coupling mechanism
  and the arterial blood pressure have equivalent effects on the model.
  The model is then used to demonstrate the interactions that arise
  between the two coupling mechanisms. We conclude by arguing that our
  approach is scalable to large numbers of nephrons, based on the
  performance characteristics of the model.
        </span>
      </li>
      <li class="renal"><a href="http://dx.doi.org/10.1098/rsta.2008.0313">A
          computational model for emergent dynamics in the kidney</a><br/>
        <span class="author">
          Robert Moss, Ed Kazmierczak, Michael Kirley, Peter Harris
        </span><br/>
        <span class="journal">
          <b>Phil. Trans. R. Soc. A</b>, 367(1896): 2125&ndash;2140, Jun 2009.
        </span><br/>
        <span class="abstract">
  Concepts from network automata are adapted and extended to model complex
  biological systems. Specifically, systems of nephrons, the operational units
  of the kidney, are modelled and the dynamics of such systems are explored. A
  network model is used to investigate the stability of systems of nephrons and
  interactions between nephrons. The intrinsic nephron control,
  tubuloglomerular feedback, is included and the effects of coupling between
  nephrons are explored in 2-, 8- and 72-nephron models.
        </span>
      </li>
      <li class="renal"><a href="http://dx.doi.org/10.1098/rsta.2008.0291">The
          Virtual Kidney: an e-Science interface and Grid Portal</a><br/>
        <span class="author">
          Peter J. Harris, Rajkumar Buyya, Xingchen Chu, Tom Kobialka,
          Ed Kazmierczak, Robert Moss, William Appelbe, Peter J. Hunter,
          S. Randall Thomas
        </span><br/>
        <span class="journal">
          <b>Phil. Trans. R. Soc. A</b>, 367(1896): 2141&ndash;2159, Jun 2009.
        </span><br/>
        <span class="abstract">
  The Virtual Kidney uses a web interface and distributed computing to provide
  experimental scientists and analysts with access to computational simulations
  and knowledge databases hosted in geographically separated laboratories. Users
  can explore a variety of complex models without requiring the specific
  programming environment in which applications have been developed.
        </span>
      </li>
      <li class="renal"><a
        href="http://repository.unimelb.edu.au/10187/3529">A Clockwork Kidney:
          Using hierarchical dynamical networks to model emergent dynamics in
          the kidney</a><br/>
        <span class="author">
          Robert Moss
        </span><br/>
        <span class="journal">
          <b>Ph.D. Thesis</b>, Sep 2008.
        </span><br/>
        <span class="abstract">
  The aim of this thesis is to provide a modelling approach and simulation
  framework that allows for emergent dynamics in multi-nephron systems to be
  studied. The ultimate intent of this research is to provide an approach to
  renal modelling that is capable of predicting whole-kidney function from the
  dynamics of individual nephrons, and can therefore be of practical use to
  clinicians. This work demonstrates that, for the first time, simulation of
  whole-kidney function from the dynamics of individual nephrons is tractable.
  Furthermore, the work provides a basis for predicting emergent effects of
  localised renal disease. With the continued development of this model, we hope
  that significant insight will be gained into the onset, progression and
  treatment of renal diseases.
        </span>
      </li>
</ul>

<script language="javascript">
  hide_noscript();
</script>
