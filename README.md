# Steinmetz-Dataset
 How does neural noise in the visual cortex affect the decision making process in a simple discrimination task.
 
# Background
- Neural noise and perceptual decision making has been studied in the context of fMRI, with results indicating that noise influences which decision will be made and can be predicted due to noise in the decision-making process (Rolls & Deco, 2011)
- Neural noise in the visual cortex has been shown to induce response variability, suggesting cortical network interactions between visual cortex and higher level regions (Fisher, 2015)
- Given the important and varied role of neuronal noise in perceptual decision making, we decided to investigate its role in mouse brain using the Steinmetz dataset

# Methodology
- With a primary focus on the visual cortex, neurons were sampled from this region across 20 different recording sessions to be analyzed.
- For a given session, each neuron’s firing rate was averaged across all trials with a stimulus occurring from the right and the stimulus occurring from the left, this was normalized and then further analyzed with a t-test to determine whether a neuron had a selectivity to where the stimulus occurred in the receptive field.
- Neurons that were proven to be selective were further grouped given their preferred stimuli, averaged out and their standard deviation was taken. This created a set of data for each of the 20 sessions which were used to create a 1-D Drift-Diffusion Model.
- The model used the difference between the averaged right selective neurons and the averaged left selective neurons to simulate a decision making process where a negative cumulative sum demonstrated a left choice and a positive cumulative sum demonstrated a right choice. 
The modelled response times were also compared to the real response times.

# Results
- The drift-diffusion model did not properly simulate the data for a number of suspected reasons.
- The bound used in the simulation was a free-parameter
- The activity of the visual cortical neurons aren’t a direct representation of the downstream decision making brain regions
- No relationship may even exist between the variables studied


