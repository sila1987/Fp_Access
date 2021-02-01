# Fp_Access
New querry to test Contrat and avenents
SELECT Avenants.CID, Avenants.REF, [Employés (étendus)].[Employé(e)], tblEmployees.Employee_ID, Avenants.contrat, Avenants.Du, Avenants.Au
FROM ([Employés (étendus)] INNER JOIN Avenants ON [Employés (étendus)].ID = Avenants.Employé) INNER JOIN tblEmployees ON [Employés (étendus)].Matricule = tblEmployees.Employee_ID
WHERE (((Avenants.Au) Between #1/1/2021# And #1/31/2021#))
ORDER BY Avenants.Du;
