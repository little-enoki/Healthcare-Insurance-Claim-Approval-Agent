# Health Insurance Claims Approval Agent
This repository contains a safe, fully synthetic reconstruction of a claims approval agent I developed in my previous role. The goal of the original system was to automate part of the medical claim review workflow by combining structured data validation with an LLM-based reasoning layer.

All examples, datasets, and logic in this repo are fabricated for demonstration purposes only.

---

## 🎯 What This Agent Does

The agent analyzes patient claim records and insurance policy rules to determine whether a claim should be:

- **Approved**, or  
- **Routed for Manual Review**

It performs this by validating medical codes, clinical criteria, demographic constraints, and preauthorization status.

The agent replicates how I designed the workflow, prompt, and evaluation logic in the real system — using entirely synthetic data.

---

## 🧮 Input Files

| File | Description |
|------|-------------|
| `insurance_policies.json` | Synthetic coverage rules per policy |
| `reference_codes.json` | Mapping of procedure & diagnosis codes (Synthetic) |
| `test_records.json` | Synthetic patient claims to evaluate |
| `validation_records.json` | Records used for validation scenario (Synthetic) |
| `validation_reference_results.csv` | Synthetic human-reviewed expected outcomes |

---

## 🧠 How the Agent Works (Process)

The workflow mirrors the production logic I designed:

1. **Summarize Patient Record**  
   Extract key clinical + demographic fields.

2. **Summarize Policy Guideline**  
   Load coverage criteria for the relevant policy.

3. **Perform Coverage Determination**  
   The agent evaluates the claim in this exact sequence:
   - Procedure code match  
   - Diagnosis code match  
   - Age range validation  
   - Gender requirement validation  
   - Preauthorization requirement  

4. **Record Pass/Fail for each step**

5. **Final Decision**  
   - All Pass → **Approve**  
   - Any Fail → **Route for Review**

6. **Export results** (Excel)

---

## 💡 Why This Matters

While no proprietary data or logic is shared, this demonstrates my:

➜ Health insurance domain expertise  
➜ ML + rule-based workflow design  
➜ Collaboration with engineering and data science teams  
➜ Experience validating agent performance using reference data
- Clear decision rules and validation logic  
- Ability to build human-vs-agent validation pipelines  

