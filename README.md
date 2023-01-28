# Aneurysm-Segmentation

This challenge is done in a course at the school of Mines Paris. **First price Winners! 1/33**

An intracranial aneurysm (IA) is a weakened or thinned portion of a blood vessel in the brain that bulges dangerously and fills up with blood, which can compress surrounding nerves and brain tissue and have a high risk of rupture. The process of identifying aneurysms requires manual identification by medical experts, taking several minutes per case. Automating this process is a worthwhile venture, which can also open up new avenues for research through obtaining large segmented datasets. Deep learning techniques are becoming popular in medical image processing and one proposed model takes a surface model of an entire set of principal brain arteries containing aneurysms as input and returns aneurysm surfaces as output.

## What about the challenge? 
Dataset:
- 105 scans (3D images)
- Size is about 3cm x 7cm x 7cm
- A small dataset as always in the medical field

The idea:
- Precise segmentation of pre-detected aneurysms
- Working on real-life data, fresh from the hospital

The main challenge is the low number of training data, to teach the network, and the complexity and size of the data we have (storage problem). the input images are 192 by 192 by 64, we cannot load all of that into the memory. We will divide these into patches of 64 by 64 by 64, we train the model on these patches, we load the next volume , then train the model then so on.
