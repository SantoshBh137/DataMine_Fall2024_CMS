Week 3 content on reconstruction of Z boson with basic cuts
This is how z1.mass and z2.mass is extracting mass 
# Extract energy and 3-momentum for each Z candidate
    #E_z1 = z1[0]
    #px_z1, py_z1, pz_z1 = z1[1], z1[2], z1[3]
    #E_z2 = z2[0]
    #px_z2, py_z2, pz_z2 = z2[1], z2[2], z2[3]

    # Compute the invariant mass using m^2 = E^2 - (px^2 + py^2 + pz^2)
    #z1_mass = np.sqrt(E_z1**2 - (px_z1**2 + py_z1**2 + pz_z1**2))
    #z2_mass = np.sqrt(E_z2**2 - (px_z2**2 + py_z2**2 + pz_z2**2))
    #z1.mass is essentially doing this 
