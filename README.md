# AM_synthesis_thesis_results

This repository contains the results of the Activation Maximisation experiments in the PhD thesis. The details about the content of each folder are mentioned below.

1. Directory - hyper_param_search_onm
   
   a) Contains the results of the experiments 1 and 2 that use the proposed FID-based evaluation metric to select the best hyper-parameter configurations.
   
      -  Experiment 1 synthesises Mel-spectrograms to minimally activate the single output layer neuron in SVDNet-R1
   
      -  Experiment 2 synthesises Mel-spectrograms to maximally activate the single output layer neuron in SVDNet-R1

2. Directory - max_min_onm
   
   a) Contains the results for the experiment 3 that uses three configurations (the best and median from the experiment 2 and the best from the experiment 1) from the previous experiments to maximise and minimise the single output layer neuron in SVDNet-R1 to understand the high-level concepts it learns.
   
3. Directory - hyper_param_search_tnm

   a) Contains the results of experiment 4 that uses the FID metric to analyse the hyper_parameter configurations for maximally activating the non-vocal (index = 0) and vocal (index=1) neurons in the output layer of the two neuron model.
   
4. Directory - comp_onm_tnm

   a) Contains the results of experiments to compare the interpretability of examples synthesised for SVDNet-R1 and SVDNet-R2 models. Two experiments are performed to analyse the interpretability of synthesised examples. The first experiment compares Mel-spectrograms synthesised by minimally activating the output layer neuron in SVDNet-R1 with examples synthesised to maximally activate the non-vocal neuron in SVDNet-R2. The second experiment compares examples to maximally activate the output neuron in SVDNet-R1 with examples that maximally activate the vocal neuron in SVDNet-R2.

======================================

Details of the files in each directory

======================================

Each seed provides a Gaussian noise vector that the experiments iteratively optimises. For each seed, there exists five files, details of which are mentioned below.

1. recon_mel_max.wav - temporal representation of the sythesised example (Mel-spectrogram).

2. noise_L2_norm.pdf - plots the L2 norm of the noise vector at each optimisation step.

3. neuron_score.pdf - plots the pre-sigmoidal activation of the output layer neuron in SVDNet-R1 at each optimisation step.

4. grad_L2_norm.pdf - plots the L2 norm of the gradient vector at each optimisation step.

5. example_iteration0_scorexyz.pdf - visualisation of the Mel-spectrogram of the synthesised example. Score refers to the pre-sigmoidal activation of the output neuron corresponding to the synthesised example. CAUTION - iteration number is incorrectly mentioned 0 in all the examples. Please ignore this. Moreover, some visualisations are normalised to [0, 1] range, but some are not.

============

Miscellanous

============

1. optm_stats_Adam.csv files are provided in some directories. They summarise the optimisation results for a configuration setting.

2. lr, rp, iter, and FID refer to the learning rate, regularisation parameter, iterations, and Frechet inception distance.
