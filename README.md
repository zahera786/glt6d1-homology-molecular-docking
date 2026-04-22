# 🧬 Homology Modeling & Molecular Docking Studies of GLT6D1

> **Computational Drug Discovery | PG Diploma Dissertation**  
> Osmania University, Hyderabad | 2021–2022  
> Supervisor: Dr. Someswar R. Sagurthi

---

## 📌 Overview

This project performs an **end-to-end in-silico drug discovery pipeline** targeting **GLT6D1 (Glycosyltransferase6 Domain1)** — a protein associated with **periodontitis (gum disease)**. Since no experimental 3D structure of GLT6D1 was available, a homology model was built computationally and used for molecular docking to identify potential drug candidates.

---

## 🎯 Objectives

- Retrieve GLT6D1 protein sequence from NCBI and identify homologous templates using BLAST
- Build a 3D homology model of GLT6D1 using **MODELLER**
- Validate the model using **PROCHECK** (Ramachandran plot analysis)
- Perform molecular docking with **10 ligands** using **AutoDock**
- Evaluate binding affinity (ΔG), inhibition constants (Ki), and drug-likeness (Lipinski's Rule of Five)

---

## 🔬 About GLT6D1

| Property | Detail |
|---|---|
| **Protein** | Glycosyltransferase6 Domain1 (GLT6D1) |
| **UniProt ID** | Q7Z4J2 (Human), Q4R5T7 (Macaca) |
| **Function** | Glycosyltransferase enzyme — transfers sugar moieties to proteins |
| **Disease Link** | Associated with **periodontitis** (gum disease) |
| **Drug Target** | Potential inhibition may aid periodontal therapy |

---

## 🛠️ Tools & Software

| Tool | Purpose |
|---|---|
| **NCBI BLAST** | Template search & sequence retrieval |
| **MODELLER** | 3D homology model construction |
| **PROCHECK** | Model validation (Ramachandran plot) |
| **AutoDock** | Molecular docking simulations |
| **PyMOL** | 3D structure visualization |
| **BIOVIA Discovery Studio** | 2D interaction maps & binding analysis |
| **PubChem** | Ligand structure & property retrieval |
| **SCFBIO** | Active site prediction |

---

## 🔄 Workflow Pipeline

```
1. Sequence Retrieval (NCBI)
        ↓
2. Template Search (BLAST → PDB)
        ↓
3. Homology Modeling (MODELLER)
        ↓
4. Model Validation (PROCHECK — Ramachandran Plot)
        ↓
5. Active Site Prediction (SCFBIO)
        ↓
6. Ligand Preparation (PubChem → 10 ligands)
        ↓
7. Molecular Docking (AutoDock)
        ↓
8. Results Analysis (Binding Energy, Ki, Drug-likeness)
```

---

## 💊 Ligands Screened

| # | Ligand Name | PubChem CID | Type |
|---|---|---|---|
| 1 | 5-(Cyclohexanecarboxamido)-2-(phenylamino)thiazole-4-carboxamide | 46355372 | Experimental |
| 2 | N-cyclopropyl-2,4-difluoro-5-((2-(pyridin-2-ylamino)thiazol-5-yl)methylamino)benzamide | 11632737 | Synthetic |
| 3 | Castanospermine | 54445 | Natural |
| 4 | Costunolide | 5281437 | Natural |
| 5 | (E)-2-(2-(4-(3-(4-bromophenyl)acrylamido)-3-fluorophenyl)benzo[d]oxazol-5-yl)acetic acid | 44402523 | Synthetic |
| 6 | N-(2-benzamido-1,3-benzothiazol-6-yl)adamantane-1-carboxamide | 4096211 | Synthetic |
| 7 | Narciclasine | 72376 | Alkaloid |
| 8 | 3,4-Dichloro-1-benzothiophene-2-carbohydrazide | 874733 | Synthetic |
| 9 | Fenclonine | 4652 | Synthetic |
| 10 | Methyl 1-hydroxy-6-phenyl-4-(trifluoromethyl)-1H-indole-2-carboxylate | 51355147 | Synthetic |

> Docked against **Q7Z4J2 (Human)** and **Q4R5T7 (Macaca)** templates  
> Active site predicted via **SCFBIO**

---

## ✅ Model Validation Results

Two homology models were built and validated using PROCHECK:

| Model | Template | Favoured Regions | Allowed Regions | Disallowed Regions |
|---|---|---|---|---|
| Model 1 | Q7Z4J2 (Human) | **92.3%** ⭐ | 7.3% | **0.0%** ✅ |
| Model 2 | Q4R5T7 (Macaca) | **88.3%** | 10.3% | **0.0%** ✅ |

> 📌 PROCHECK standard: a good quality model should have **>90% residues in favoured regions**  
> Model 1 exceeds this threshold — confirming **high model quality**

---

## 🏆 Key Docking Results

### Best Result — Ligand 1 (CID: 46355372)

| Property | Value |
|---|---|
| **Ligand** | Cyclohexanecarboxamide derivative |
| **Binding Energy (ΔG)** | **−9.34 kcal/mol** |
| **Inhibition Constant (Ki)** | **142.16 nM** |
| **Protein Template** | Q7Z4J2 (Human) |
| **Key Residues** | TRP39 · LYS2 · GLU33 · ALA3 |
| **Interaction Types** | Conventional H-Bond, Pi-Pi Stacked |

### All Docking Results Summary

| Ligand CID | Protein | Binding Energy (ΔG) | Ki |
|---|---|---|---|
| 46355372 | Q7Z4J2 | **−9.34 kcal/mol** | 142.16 nM |
| 46355372 | Q4R5T7 | −8.30 kcal/mol | 822.73 μM |
| 11632737 | Q7Z4J2 | −8.46 kcal/mol | 627.97 nM |
| 11632737 | Q4R5T7 | −7.76 kcal/mol | 2.06 μM |
| 54445 | Q7Z4J2 | −5.36 kcal/mol | 117.72 μM |
| 5281437 | Q7Z4J2 | −6.73 kcal/mol | 11.59 μM |
| 44402523 | Q7Z4J2 | −9.10 kcal/mol | 213.98 nM |
| 4096211 | Q7Z4J2 | −11.09 kcal/mol | 7.39 nM |
| 72376 | Q7Z4J2 | −6.54 kcal/mol | 15.97 μM |
| 874733 | Q7Z4J2 | −7.00 kcal/mol | 7.45 μM |

---

## 💊 Drug-Likeness Analysis (Lipinski's Rule of Five)

All 10 ligands were evaluated for oral bioavailability using **Lipinski's Rule of Five**:

| Property | Criteria | Result |
|---|---|---|
| Molecular Weight | ≤ 500 g/mol | ✅ Compliant |
| LogP (Lipophilicity) | ≤ 5 | ✅ Compliant |
| H-Bond Donors | ≤ 5 | ✅ Compliant |
| H-Bond Acceptors | ≤ 10 | ✅ Compliant |
| Lipinski Violations | 0 | ✅ Most ligands |

> All screened ligands show good drug-likeness properties and potential for oral bioavailability.

---

## 📊 Results Visualization

The project includes:
- **Ramachandran plots** — model validation for both templates
- **PyMOL 3D visualizations** — protein-ligand binding poses
- **BIOVIA 2D interaction maps** — hydrogen bond and hydrophobic interaction diagrams
- **Docking tables** — binding energies and Ki values for all 10 ligands

---

## 🧪 Conclusion

- ✅ A reliable **3D homology model of GLT6D1** was successfully built and validated
- ✅ **Cyclohexanecarboxamide derivative (CID: 46355372)** showed the best binding energy of **−9.34 kcal/mol** (Ki = 142.16 nM)
- ✅ All ligands satisfied **Lipinski's Rule of Five**, confirming drug-likeness
- ✅ These lead compounds are candidates for **further experimental validation** and drug development against periodontitis

---

## 👩‍🔬 Author

**Zahera Fathima Khatoon**  
Roll No: 094224010028  
PG Diploma in Bioinformatics  
Osmania University, Hyderabad | 2021–2022

🔗 [LinkedIn](https://linkedin.com/in/zahera-khatoon-9598382a0) · [GitHub](https://github.com/zahera786)

---

## 📚 References

1. Lairson LL, Henrissat B, Davies GJ, Withers SG. Glycosyltransferases: structures, functions, and mechanisms. *Annu Rev Biochem.* 2008;77:521–555.
2. Krieger E, Nabuurs SB, Vriend G. Homology modeling. *Methods Biochem Anal.* 2003;44:509–24.
3. Morris GM et al. AutoDock4 and AutoDockTools4: Automated docking with selective receptor flexibility. *J Comput Chem.* 2009;30:2785–91.
4. Laskowski RA et al. PROCHECK — a program to check the stereochemical quality of protein structures. *J Appl Cryst.* 1993;26:283–291.

---

*Submitted for PG Diploma in Bioinformatics · PGRRCDE, Osmania University, Hyderabad · 2021–2022*  
*Supervised by Dr. Someswar R. Sagurthi*
