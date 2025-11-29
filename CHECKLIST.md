# AFEOL Pull Request Checklist
MIT License · UTF-8 · AFEOL Documentation Standard

This checklist must be completed before merging any pull request into the AfeolProject repository.

---

## 1. Summary Review
- [ ] PR description is clear and concise  
- [ ] Purpose of the change is explicitly stated  
- [ ] No missing explanations or vague motivations

---

## 2. Code Quality
- [ ] Code follows AFEOL Coding Standard  
- [ ] No commented-out dead code  
- [ ] No debug prints, temporary logs, or leftover test blocks  
- [ ] No unnecessary file changes or formatting noise  
- [ ] File structure and naming follow AFEOL rules

---

## 3. Documentation & Metadata
- [ ] Documentation updated if needed  
- [ ] CHANGELOG.md updated if relevant  
- [ ] No sensitive data added  
- [ ] English is the primary language of all new text  
- [ ] Commit messages follow AFEOL commit style

---

## 4. Security Review
- [ ] No secrets, keys, tokens, or identifiers included  
- [ ] No telemetry, analytics, or tracking  
- [ ] No dependency adds without verification  
- [ ] Changes respect privacy/anonymity principles  
- [ ] No JavaScript added (unless explicitly approved by AFEOL policy)

---

## 5. Functional Integrity
- [ ] Change compiles / runs without errors  
- [ ] Tested locally (manual or automated)  
- [ ] No regressions introduced  
- [ ] All modified modules behave as expected

---

## 6. Repository Structure
- [ ] No accidental file moves or renames  
- [ ] No binary files added unless intentional  
- [ ] No unnecessary root-level files

---

## 7. Branch Workflow Compliance
- [ ] PR is from feature/fix/docs branch (not from main)  
- [ ] PR targets the `dev` branch  
- [ ] Branch name follows AFEOL GitHub Workflow (feature-x, fix-x, docs-x)

---

## 8. Final Validation
- [ ] I confirm I have reviewed every section above  
- [ ] I approve this PR according to AFEOL GitHub Workflow v1.0  
- [ ] The PR is ready to be merged

---

**Reviewer Signature:**  
`@AfeolProject`
