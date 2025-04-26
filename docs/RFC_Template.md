```markdown
# RFC Template: OpenColor Standard (OCS)

---
**RFC Title**: [Brief descriptive title, e.g., "Add Fluorescent Colors"]  
**Author**: [Your GitHub username]  
**Date**: YYYY-MM-DD  
**Status**: Draft | Proposed | Rejected | Implemented  
**Discussions**: [GitHub Issue or Forum Thread URL]  

---

## 1. Motivation  
*Why is this change needed?*  
- Example:  
  > "Fluorescent colors are widely used in packaging but currently require Pantone spot inks. Adding them to OCS would reduce dependency on proprietary systems."

---

## 2. Proposal  
*Technical description of the change.*  

### For New Colors:  
```ocs
OCS-[ID]-[C]-[M]-[Y]-[K]-[O]-[G]-[F]  # F = Fluorescent (0-1000g)
```

**Base Ink Definition**:  
- `F1`: Fluorescent Pink (CIELAB `L=85, a=40, b=-10`)  
- `F2`: Fluorescent Orange (CIELAB `L=80, a=50, b=70`)  

### For Tools:  
- [ ] Add support to `ocs-converter.py`  
- [ ] Update Inkscape plugin  

---

## 3. Alternatives Considered  
*Other approaches and why they were rejected.*  
1. *Use existing Orange/Green inks*:  
   - ❌ Cannot achieve fluorescence.  
2. *Separate "OCS-Neon" namespace*:  
   - ❌ Overcomplicates the standard.  

---

## 4. Compatibility  
*Impact on existing implementations.*  
- Backward-compatible: Old codes (`OCS-FIRE-0-800-200`) still valid.  
- New converters must handle 7-component codes.  

---

## 5. Voting  
*Community decision process.*  
- [ ] 👍 Accept  
- [ ] 👎 Reject  
- [ ] 💬 Needs revision  

*Voting ends on YYYY-MM-DD.*  

---

## 6. References  
- [Pantone Fluorescent Guide](https://www.pantone.com/fluorescent)  
- [CIELAB values for fluorescence](https://example.com)  
```
