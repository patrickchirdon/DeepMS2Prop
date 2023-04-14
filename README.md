# DeepMS2Prop

Testing data can be found in the compound*.csv files.
Must have tensorflow, rdkit, keras, scikit-learn installed, jupyter notebook, anaconda to run ms2prop2.ipynb 

-------------------------------------------------------------------------------------------------
MS testing data can be found  here: https://massbank.eu/MassBank/
training data from https://gnps.ucsd.edu/ProteoSAFe/static/gnps-splash.jsp

Mass Spectroscopy Peaks to Properties Prediction

Overview of Phase 0 of a Clinical Trial Phase 0 of a clinical trial before animal testing is a combination of Autodock Vina or Rosetta docking with protein structures from Alphafold, Meta, or RCSB. Quantitative Structure Activity Relationship (QSAR) modeling using machine learning, typically in rdkit or scikitlearn or keras, screens molecules for inhibition or activation using chembl or pubchem databases typically prior to protein ligand docking. QSAR modeling uses chembl or pubchem databases, using inhibitory IC50 or activation data collected from experiments. Molecules can be generated from chemical scaffolds, keeping the core scaffold the same and modifying only the R groups, using Data Warrior. Data Warrior stores chemical data and can screen for basic physical or toxicity properties, as well as providing a visualization for datasets. Molecules are represented in SMILES format. In addition to QSAR modeling, the SMILES molecules can be filtered for substructures called SMARTS. SMARTS are useful for rule based models in organic chemistry. Rule based models are the traditional alternative to machine learning based approaches. Structural alerts are the smallest possible substructure within a molecule having a biological activity and can be found in the literature or from databases like ochem.eu. However, sometimes the chemical structure is not known. In these cases, software like MSNovelist can guess the structures from mass spectroscopy data.


ADMET Screening 

As an initial first screen, software libraries screen for adsorption, distribution, metabolism, and excretion properties (ADMET) using online sources like SwissADME or ADMETlab2.0. Toxicity modeling is done with QSAR modeling in rdkit or using models like Tox21 from Deepchem. Although some might argue that predicting accurately how compounds travel through the body is equivalent to the feat of landing someone on Mars, in silico screens are useful for predicting which compounds are not suitable for preclinical testing. Many compounds are not able to cross the blood brain barrier, are not transported well in the blood, distributed to various compartments of the body, or are unable to pass through the stomach or intestines. The liver metabolizes these compounds and they are often not able to reach the target site. Predicting how compounds are metabolized in the liver by cytochromes prior to experiments is often useful, as is predicting transport with plasma proteins, volume of distribution, intestinal absorption, GI absorption, and half life, or renal clearance. Ideally, after in silico screening the goal is to have all the possible conformations of a scaffold generated with all the adsorption, metabolism, excretion, and toxicity data predicted for each compound with bioactivity scores and protein ligand binding energy scores so that the compounds can be prioritized. Bad compounds never leave the computer, potentially saving costly experiments and time. Prior to phases 1-3 of a clinical study, a preclinical study is necessary to assess toxicity and other properties of the best compounds. This can be done at labs like Charles River or using animal models. Phases 1-3 of a clinical study assess safety and efficacy of a drug. These are performed at hospital systems by contract research organizations such as Trialspark, etc that match academic labs and compounds to pharmaceutical companies. There is a high failure rate of clinical trials and in many cases the trials cost almost a billion dollars and 10 years to complete.

The Role of Small Chemical Companies

Biosortia, like many companies, did not know the structures of their compounds and had only mass spectroscopy data.  The mass spectroscopy data could be converted to chemical structures using MSNovelist in order to perform protein ligand docking. We also wanted to predict chemical properties for adsorption, distribution, metabolism, and excretion. Rather than using SMILES for QSAR models, we went directly from mass spectroscopy peaks to properties with high accuracy.  The assay data could come from Chembl or Pubchem.  However, most of our ADME model data came from the popular adsorption, metabolism, excretion, and transport prediction software named ADMETlab2.0.  We wanted to note that going directly from mass spectroscopy peaks is under-published, with only one company Enveda Bio publishing Ms2Prop at the time of writing.  

Resources

https://www.rosettacommons.org/

https://openmolecules.org/datawarrior/

https://admetmesh.scbdd.com/

https://chatgpdb-ambermd.org

https://www.rcsb.org/

https://chemicbook.com/2023/04/11/LLMs-in-Chemistry.html
