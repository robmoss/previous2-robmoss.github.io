---
title: Publications
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
        to_hide = document.getElementsByClassName("abstract");
        for (var i = 0; i < to_hide.length; i++) {
          to_hide[i].style["display"] = "none";
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

<ul class="publication-list">
      <li class="epi"><a
        href="https://doi.org/10.1186/s12889-019-6968-x">What can urban
        mobility data reveal about the spatial distribution of infection in a
        single city?</a><br/>
        <span class="author">Moss R, Naghizade E, Tomko M, Geard N</span><br/>
        <span class="journal"><b>BMC Public Health</b>
        19: 656, Mar 2019</span><br/>
        <span class="abstract">
        <strong>Background:</strong>
        Infectious diseases spread through inherently spatial processes. Road
        and air traffic data have been used to model these processes at
        national and global scales. At metropolitan scales, however, mobility
        patterns are fundamentally different and less directly observable.
        Estimating the spatial distribution of infection has public health
        utility, but few studies have investigated this at an urban scale. In
        this study we address the question of whether the use of urban-scale
        mobility data can improve the prediction of spatial patterns of
        influenza infection. We compare the use of different sources of
        urban-scale mobility data, and investigate the impact of other factors
        relevant to modelling mobility, including mixing within and between
        regions, and the influence of hub and spoke commuting patterns.
        <br/><strong>Methods:</strong>
        We used journey-to-work (JTW) data from the Australian 2011 Census,
        and GPS journey data from the Sygic GPS Navigation & Maps mobile app,
        to characterise population mixing patterns in a spatially-explicit
        SEIR (susceptible, exposed, infectious, recovered) meta-population
        model.
        <br/><strong>Results:</strong>
        Using the JTW data to train the model leads to an increase in the
        proportion of infections that arise in central Melbourne, which is
        indicative of the city’s spoke-and-hub road and public transport
        networks, and of the commuting patterns reflected in these data. Using
        the GPS data increased the infections in central Melbourne to a lesser
        extent than the JTW data, and produced a greater heterogeneity in the
        middle and outer regions. Despite the limitations of both mobility
        data sets, the model reproduced some of the characteristics observed
        in the spatial distribution of reported influenza cases.
        <br/><strong>Conclusions:</strong>
        Urban mobility data sets can be used to support models that capture
        spatial heterogeneity in the transmission of infectious diseases at a
        metropolitan scale. These data should be adjusted to account for
        relevant urban features, such as highly-connected hubs where the
        resident population is likely to experience a much lower force of
        infection that the transient population. In contrast to national and
        international scales, the relationship between mobility and infection
        at an urban level is much less apparent, and requires a richer
        characterisation of population mobility and contact.
        </span>
      </li>
      <li class="epi"><a
        href="https://doi.org/10.33321/cdi.2019.43.7">Anatomy of a seasonal
        influenza epidemic forecast</a><br/>
        <span class="author">Moss R, Zarebski AE, Dawson P, Franklin LJ,
        Birrell FA, McCaw JM</span><br/>
        <span class="journal"><b>Communicable Diseases Intelligence</b>
        43: 1&ndash;14, Mar 2019</span><br/>
        <span class="abstract">
        Bayesian methods have been used to predict the timing of infectious
        disease epidemics in various set-tings and for many infectious
        diseases, including seasonal influenza. But integrating these
        techniques into public health practice remains an ongoing challenge,
        and requires close collaboration between modellers, epidemiologists,
        and public health staff.
        <br/><br/>
        During the 2016 and 2017 Australian influenza seasons, weekly seasonal
        influenza forecasts were produced for cities in the three states with
        the largest populations: Victoria, New South Wales and Queensland.
        Forecast results were presented to Health Department disease
        surveillance units in these jurisdictions, who provided feedback about
        the plausibility and public health utility of these predictions.
        <br/><br/>
        In earlier studies we found that delays in reporting and processing of
        surveillance data substantially limited forecast performance, and that
        incorporating climatic effects on transmission improved forecast
        performance. In this study of the 2016 and 2017 seasons, we sought to
        refine the forecasting method to account for delays in receiving the
        data, and used meteorological data from past years to modulate the
        force of infection. We demonstrate how these refinements improved the
        forecast's predictive capacity, and use the 2017 influenza season to
        highlight challenges in accounting for popu-lation and clinician
        behaviour changes in response to a severe season.
        </span>
      </li>
      <li class="epi"><a
        href="https://doi.org/10.3390/tropicalmed4010012">Accounting for
        healthcare-seeking behaviours and testing practices in real-time
        influenza forecasts</a><br/>
        <span class="author">Moss R, Zarebski AE, Carlson SJ,
        McCaw JM</span><br/>
        <span class="journal"><b>Tropical Medicine and Infectious Disease</b>
        4(1): 12, Jan 2019</span><br/>
        <span class="abstract">
        For diseases such as influenza, where the majority of infected persons
        experience mild (if any) symptoms, surveillance systems are sensitive
        to changes in healthcare-seeking and clinical decision-making
        behaviours. This presents a challenge when trying to interpret
        surveillance data in near-real-time (e.g., to provide public health
        decision-support). Australia experienced a particularly large and
        severe influenza season in 2017, perhaps in part due to: (a) mild
        cases being more likely to seek healthcare; and (b) clinicians being
        more likely to collect specimens for reverse transcription polymerase
        chain reaction (RT-PCR) influenza tests. In this study, we used weekly
        Flutracking surveillance data to estimate the probability that a
        person with influenza-like illness (ILI) would seek healthcare and
        have a specimen collected. We then used this estimated probability to
        calibrate near-real-time seasonal influenza forecasts at each week of
        the 2017 season, to see whether predictive skill could be improved.
        While the number of self-reported influenza tests in the weekly
        surveys are typically very low, we were able to detect a substantial
        change in healthcare seeking behaviour and clinician testing behaviour
        prior to the high epidemic peak. Adjusting for these changes in
        behaviour in the forecasting framework improved predictive skill. Our
        analysis demonstrates a unique value of community-level surveillance
        systems, such as Flutracking, when interpreting traditional
        surveillance data. These methods are also applicable beyond the
        Australian context, as similar community-level surveillance systems
        operate in other countries.
        </span>
      </li>
      <li class="epi"><a
        href="http://dx.doi.org/10.1111/1753-6405.12750">Epidemic forecasts as
        a tool for public health: interpretation and (re)calibration</a><br/>
        <span class="author">Moss R, Fielding JE, Franklin LJ, Stephens N,
        McVernon J, Dawson P, McCaw JM</span><br/>
        <span class="journal"><b>Australian and New Zealand Journal of Public
        Health</b> 42(1): 69&ndash;76, Feb 2018</span><br/>
        <span class="abstract">
        <strong>Objective and Methods:</strong> Recent studies have used
        Bayesian methods to predict timing of influenza epidemics many weeks
        in advance, but there is no documented evaluation of how such
        forecasts might support the day-to-day operations of public health
        staff. During the 2015 influenza season in Melbourne, Australia,
        weekly forecasts were presented at Health Department surveillance unit
        meetings and evaluated and updated in light of expert opinion, to
        improve their accuracy and usefulness.
        <br/><strong>Results:</strong> Predictive capacity of the model was
        substantially limited by delays in reporting and processing arising
        from an unprecedented number of notifications, disproportionate to
        seasonal intensity. Adjustment of the predictive algorithm to account
        for these delays and increased reporting propensity improved both
        current situational awareness and forecasting accuracy.
        <br/><strong>Conclusions:</strong> Collaborative engagement with
        public health practitioners in model development improved
        understanding of the context and limitations of emerging surveillance
        data. Incorporation of these insights in a quantitative model resulted
        in more robust estimates of disease activity for public health use.
        <br/><strong>Implications for Public Health:</strong> In addition to
        predicting future disease trends, forecasting methods can quantify the
        impact of delays in data availability and variable reporting practice
        on the accuracy of current epidemic assessment. Such evidence supports
        investment in systems capacity.
        </span>
      </li>
      <li class="epi"><a
        href="http://dx.doi.org/10.1016/j.idm.2016.12.004">Model selection for
        seasonal influenza forecasting</a><br/>
        <span class="author">
          Zarebski AE, Dawson P, McCaw JM, Moss R
        </span><br/>
        <span class="journal">
          <b>Infect Dis Mod</b> 2(1): 56&ndash;70, Feb 2017
        </span><br/>
        <span class="abstract">
        Epidemics of seasonal influenza inflict a huge burden in temperate
        climes such as Melbourne (Australia) where there is also significant
        variability in their timing and magnitude. Particle filters combined
        with mechanistic transmission models for the spread of influenza have
        emerged as a popular method for forecasting the progression of these
        epidemics. Despite extensive research it is still unclear what the
        optimal models are for forecasting influenza, and how one even
        measures forecast performance.<br/><br/>
        In this paper, we present a likelihood-based method, akin to Bayes
        factors, for model selection when the aim is to select for predictive
        skill. Here, "predictive skill" is measured by the probability of the
        data after the forecasting date, conditional on the data from before
        the forecasting date. Using this method we choose an optimal model of
        influenza transmission to forecast the number of laboratory-confirmed
        cases of influenza in Melbourne in each of the 2010-15 epidemics. The
        basic transmission model considered has the
        susceptible-exposed-infectious-recovered structure with extensions
        allowing for the effects of absolute humidity and inhomogeneous mixing
        in the population. While neither of the extensions provides a
        significant improvement in fit to the data they do differ in terms of
        their predictive skill. Both measurements of absolute humidity and a
        sinusoidal approximation of those measurements are observed to
        increase the predictive skill of the forecasts, while allowing for
        inhomogeneous mixing reduces the skill.<br/><br/>
        We discuss how our work could be integrated into a forecasting system
        and how the model selection method could be used to evaluate forecasts
        when comparing to multiple surveillance systems providing disparate
        views of influenza activity.
        </span>
      </li>
      <li class="epi"><a
        href="http://dx.doi.org/10.1017/S0950268816002053">Retrospective
        forecasting of the 2010&ndash;2014 Melbourne influenza seasons using
        multiple surveillance systems</a><br/>
        <span class="author">
          Moss R, Zarebski A, Dawson P, McCaw JM
        </span><br/>
        <span class="journal">
          <b>Epidemiol Infect</b> 145(1): 156&ndash;169, Jan 2017.
        </span><br/>
        <span class="abstract">
        Accurate forecasting of seasonal influenza epidemics is of great
        concern to healthcare providers in temperate climates, since these
        epidemics vary substantially in their size, timing and duration from
        year to year, making it a challenge to deliver timely and
        proportionate responses.
        Previous studies have shown that Bayesian estimation techniques can
        accurately predict when an influenza epidemic will peak many weeks in
        advance, and we have previously tailored these methods for
        metropolitan Melbourne (Australia) and Google Flu Trends data.
        Here we extend these methods to clinical observation and
        laboratory-confirmation data for Melbourne, on the grounds that these
        data sources provide more accurate characterizations of influenza
        activity.
        We show that from each of these data sources we can accurately predict
        the timing of the epidemic peak 4-6 weeks in advance.
        We also show that making simultaneous use of multiple surveillance
        systems to improve forecast skill remains a fundamental challenge.
        Disparate systems provide complementary characterizations of disease
        activity, which may or may not be comparable, and it is unclear how a
        "ground truth" for evaluating forecasts against these multiple
        characterizations might be defined.
        These findings are a significant step towards making optimal use of
        routine surveillance data for outbreak forecasting.
        </span>
      </li>
      <li class="epi"><a
        href="http://dx.doi.org/10.1186/s12879-016-1866-7">Reducing disease
        burden in an influenza pandemic by targeted delivery of neuraminidase
        inhibitors: mathematical models in the Australian context</a><br/>
        <span class="author">
          Moss R, McCaw JM, Cheng AC, Hurt AC, McVernon J
        </span><br/>
        <span class="journal">
          <b>BMC Infect Dis</b> 16(1): 552, Oct 2016.
        </span><br/>
        <span class="abstract">
        <strong>Background:</strong> Many nations maintain stockpiles of
        neuraminidase inhibitor (NAI) antiviral agents for use in influenza
        pandemics to reduce transmission and mitigate the course of clinical
        infection. Pandemic preparedness plans include the use of these
        stockpiles to deliver proportionate responses, informed by emerging
        evidence of clinical impact. Recent uncertainty about the
        effectiveness of NAIs has prompted these nations to reconsider the
        role of NAIs in pandemic response, with implications for pandemic
        planning and for NAI stockpile size.
        <br/><strong>Methods:</strong> We combined a dynamic model of
        influenza epidemiology with a model of the clinical care pathways in
        the Australian health care system to identify effective NAI
        strategies for reducing morbidity and mortality in pandemic events,
        and the stockpile requirements for these strategies. The models were
        informed by a 2015 assessment of NAI effectiveness against
        susceptibility, pathogenicity, and transmission of influenza.
        <br/><strong>Results:</strong> Liberal distribution of NAIs for early
        treatment in outpatient settings yielded the greatest benefits in all
        of the considered scenarios. Restriction of community-based treatment
        to risk groups was effective in those groups, but failed to prevent
        the large proportion of cases arising from lower risk individuals who
        comprise the majority of the population.
        <br/><strong>Conclusions:</strong> These targeted strategies are only
        effective if they can be deployed within the constraints of existing
        health care infrastructure. This finding highlights the critical
        importance of identifying optimal models of care delivery for
        effective emergency health care response.
        </span>
      </li>
      <li class="epi"><a
        href="http://dx.doi.org/10.1371/journal.pntd.0005018">Model-informed
        risk assessment and decision making for an emerging infectious disease
        in the Asia-Pacific region</a><br/>
        <span class="author">
          Moss R, Hickson RI, McVernon J, McCaw JM, Hort K, Black J,
          Madden JR, Tran NH, McBryde ES, Geard N
        </span><br/>
        <span class="journal">
          <b>PLoS Negl Trop Dis</b> 10(9): e0005018, Sep 2016.
        </span><br/>
        <span class="abstract">
        <strong>Background:</strong> Effective response to emerging infectious
        disease (EID) threats relies on health care systems that can detect
        and contain localised outbreaks before they reach a national or
        international scale.
        The Asia-Pacific region contains low and middle income countries in
        which the risk of EID outbreaks is elevated and whose health care
        systems may require international support to effectively detect and
        respond to such events.
        The absence of comprehensive data on populations, health care systems
        and disease characteristics in this region makes risk assessment and
        decisions about the provision of such support challenging.
        <br/><strong>Methodology/principal findings:</strong> We describe a
        mathematical modelling framework that can inform this process by
        integrating available data sources, systematically explore the effects
        of uncertainty, and provide estimates of outbreak risk under a range
        of intervention scenarios.
        We illustrate the use of this framework in the context of a potential
        importation of Ebola Virus Disease into the Asia-Pacific region.
        Results suggest that, across a wide range of plausible scenarios,
        preemptive interventions supporting the timely detection of early
        cases provide substantially greater reductions in the probability of
        large outbreaks than interventions that support health care system
        capacity after an outbreak has commenced.
        <br/><strong>Conclusions/significance</strong> Our study demonstrates
        how, in the presence of substantial uncertainty about health care
        system infrastructure and other relevant aspects of disease control,
        mathematical models can be used to assess the constraints that limited
        resources place upon the ability of local health care systems to
        detect and respond to EID outbreaks in a timely and effective fashion.
        Our framework can help evaluate the relative impact of these
        constraints to identify resourcing priorities for health care system
        support, in order to inform principled and quantifiable decision
        making.
        </span>
      </li>
      <li class="epi"><a
        href="http://dx.doi.org/10.1111/irv.12376">Forecasting influenza
        outbreak dynamics in Melbourne from Internet search query surveillance
        data</a><br/>
        <span class="author">
           Moss R, Zarebski A, Dawson P, McCaw JM
        </span><br/>
        <span class="journal">
          <b>Influenza Other Respir Viruses</b> 10(4): 314&ndash;323, Jul 2016
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
           Cao P, Yan AWC, Heffernan JM, Petrie S, Moss R, Carolan LA,
           Guarnaccia TA, Kelso A, Barr IG, McVernon J, Laurie KL, McCaw JM
        </span><br/>
        <span class="journal">
          <b>PLoS Comp Biol</b> 11(8): e1004334, Aug 2015
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
          <b>PLoS Comp Biol</b> 8(6): e1002571, Jun 2012.
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
  tailoring to the country's infrastructural and sociobehavioural
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
          Hernández AI, Le Rolle V, Ojeda D, Baconnier P, Fontecave-Jallon J,
          Guillaud F, Grosse T, Moss R, Hannaert P, Thomas SR
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
          McCaw JM, Moss R, McVernon J
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
  scenarios given Australia's existing public health capacities. We then
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
          Moss R, McCaw JM, McVernon J
        </span><br/>
        <span class="journal">
          <b>PLoS ONE</b> 6(2): e14505, Feb 2011.
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
          Moss R, Kazmierczak E, Kirley M, Harris PJ
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
          Moss R, Kazmierczak E, Kirley M, Harris PJ
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
          Harris PJ, Buyya R, Chu X, Kobialka T, Kazmierczak E, Moss R,
          Appelbe W, Hunter PJ, Thomas SR
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
          Moss R
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
