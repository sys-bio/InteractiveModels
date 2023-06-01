# InteractiveModels
Models and simulator for Interactive modeling site: https://sites.google.com/view/interactive-modeling/home 

## Adding a model to the Interactive Modeling webpage (on Google Sites)
1. Add the SBML model to the ../models/ dir
2. Go to the Google sites page where you want the simulation to run.
3. Embeded the template code into the page:
* Template is in ../templates/sysbioTemplate.html.
* Fill out the following part of the template with model simulation details:
  // **** Simulation info to fill out: ********
  const modelURL = 'https://sys-bio.github.io/InteractiveModels/models/modelFileName.xml'; // Location of sbml model file on github.
  const newRT = '10';       // Length of run in model time units
  const newSS = '0.10';     // integrator step size, total pts = newRt/newSS, 100 points: (10/0.10)
  const staticRun = 'true'; // Display after all calculations are done.
  const sliders = 'k1, p_3, comp1';// Sliders 12 max, exact id match, '' for first 8 params and first 4 species of model.
  const spPlot = 'S1, deS2, Oxy2'; // Species to plot, exact id match, '' for first up to 8 species.
  const yLabel = 'conc (uM)'; // Plot label, displayed at bottom as: yLabel vs. xLabel
  const xLabel = 'sec';
  // *** END of Simulation info to fill out ***
 * Insert the whole template, including the load button and iframe information into the page.
4. Save and publish page. Check page out to confirm model loads and runs as expected.
