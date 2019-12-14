# AM_audio_thesis_results

This repository contains the results of the Activation Maximisation experiments the PhD thesis. The details about the content of each folder are mentioned below.

1. Directory - hyper_param_search_onm
   
   a) Contains the results for the experiments 1 and 2 that use the proposed FID-based evaluation metric to select the best hyper-parameter configuration.
   
   b) Experiment 1 synthesises Mel-spectrograms to minimally activate the single output layer neuron in SVDNet-R1
   
   c) Experiment 2 synthesises Mel-spectrograms to maximally activate the single output layer neuron in SVDNet-R1

2. Directory - max_min_onm
   
   a) Contains the results for the experiment 3 that uses three configurations (best and median from the experiment 1 and the best from the experiment 2) from the previous experiments to maximise and minimise the single output layer neuron in SVDNet-R1. 

======================================
Details of the files in each directory
======================================

Each seed provides a Gaussian noise vector that the experiments iteratively optimise. For each seed, there exist five files details of which are mentioned below.

1. recon_mel_max.wav - temporal representation of the sythesised example(Mel-spectrogram).
2. noise_L2_norm.pdf - plots the L2 norm of the noise vector at each optimisation step.
3. neuron_score.pdf - plots the pre-sigmoidal activation of the output layer neuron in SVDNet-R1 at each optimisation step.
4. grad_L2_norm.pdf - plots the L2 norm of the gradient vector at each optimisation step.
5. example_iteration0_score7.94.pdf - visualisation of the Mel-spectrogram of the synthesised example. Score refers to the pre-sigmoidal activation of the output neuron corresponding to the synthesised example. CAUTION - iteration number is incorrectly mentioned 0 in all the examples. Please ignore this. Moreover, some visualisations are normalised to [0, 1] range, but some are not.
