Week 3 content on reconstruction of Z boson with basic cuts
This is how z1.mass and z2.mass is extracting mass 


#def compute_z_masses_2el2mu(electron_pt, electron_eta, electron_phi, electron_mass,
                            muon_pt, muon_eta, muon_phi, muon_mass):
    
    # Create Lorentz vectors for electrons and muons using awkward and vector
    electron_p4 = ak.zip({
        "pt": electron_pt,
        "eta": electron_eta,
        "phi": electron_phi,
        "mass": electron_mass
    }, with_name="PtEtaPhiMLorentzVector")
    
    muon_p4 = ak.zip({
        "pt": muon_pt,
        "eta": muon_eta,
        "phi": muon_phi,
        "mass": muon_mass
    }, with_name="PtEtaPhiMLorentzVector")

    # Convert awkward arrays to vector.Array
    electron_vec = vector.awk(ak.Array(electron_p4))
    muon_vec = vector.awk(ak.Array(muon_p4))

    # Form Z candidates by adding the appropriate four-momenta
    z1 = electron_vec[:, 0] + electron_vec[:, 1]  # First Z candidate (from electrons)
    z2 = muon_vec[:, 0] + muon_vec[:, 1]          # Second Z candidate (from muons)

    
    # Compute invariant masses
    z1_mass = z1.mass
    z2_mass = z2.mass
    
    # Extract energy and 3-momentum for each Z candidate
    #E_z1 = z1[0]
    #px_z1, py_z1, pz_z1 = z1[1], z1[2], z1[3]
    #E_z2 = z2[0]
    #px_z2, py_z2, pz_z2 = z2[1], z2[2], z2[3]

    # Compute the invariant mass using m^2 = E^2 - (px^2 + py^2 + pz^2)
    #z1_mass = np.sqrt(E_z1**2 - (px_z1**2 + py_z1**2 + pz_z1**2))
    #z2_mass = np.sqrt(E_z2**2 - (px_z2**2 + py_z2**2 + pz_z2**2))
    #z1.mass is essentially doing this 


    return z1_mass, z2_mass
