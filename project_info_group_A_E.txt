Our project this semester will be a simplified version of the Higgs analysis performed by researchers in the CMS collaboration, but even this simple version will be significantly complex and take some time to fully grasp. Specifically, we will analyze events where the Higgs boson decays to two tau leptons which decay to four leptons (muons and electrons). We will create plots showing the number of events as a function of the total mass involved in the events. These plots will be separated into three categories:
The four muon channel
The four electron channel
The two electron, two muon channel

We use both simulated events and actual data to model the decays. There are basically three steps to the process, which you will aim to recreate throughout this semester:
Apply cuts based on event properties such as transverse momentum, number of leptons, and quality of the tracks. This reduces the total events to a much smaller set of events which are likely candidates for a Higgs decay.
Reconstruct a pair of Z bosons from the events we’ve selected, then apply additional cuts on these reconstructed objects.
Reconstruct the Higgs boson from these Z bosons.
	One of the main cuts we apply in the first step is for events with low eta (angles close to perpendicular from the beams) and high pT (large transverse momentum). The reason we want events in this region is because they indicate a hard scattering event in the beams, meaning two protons collided almost head-on and produced new particles. Events with higher eta (angles closer to parallel with the beams) and lower transverse momentum are events indicating soft scattering in the beams, meaning the protons just brushed off of each other and likely did not create a Higgs boson. 
	In fact, the CMS detector has physical triggers that already select for such events (high pT, low eta) before any data analysis is done, throwing away data on soft scattering events. But these triggers are imperfect because they have too much data to process. This is why we apply further cuts during the analysis step, to further filter out uninteresting events. 
