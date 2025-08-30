---
type: Post
title: Maintaining Consistent Font Sizes in Canvas Apps
description: >-
  Standardize font sizes in Power Apps canvas apps by learning unit differences, conversion tips, and how to use variables for consistent typography.
date: '2024-02-30'
---
When creating a modern-looking canvas app, one common challenge is the mixed usage of **classic** and **modern** controls. You may notice that the text in modern controls appears smaller than in classic controls. To maintain visual consistency, it’s important to keep the font size consistent across all the app’s controls.

---

## Why the Difference?

The difference arises from the **unit of font size**:

- **Modern controls** use **pixels (px)**  
- **Classic controls** use **points (pt)**  

---

## Conversion Between Pixels and Points

- To convert **pixels (modern control)** → **points (classic control)**:  
  **Divide** the font size value by `0.75`

- To convert **points (classic control)** → **pixels (modern control)**:  
  **Multiply** the font size value by `0.75`

---

## Using Variables for Consistency

To keep font sizes consistent across the app, declare variables in the **App’s Formulas** property:

```csharp
varFontSizeClassic = 13;
varFontSizeModern = varFontSizeClassic * 0.75;
```

### How to Use
- When adding a **modern control**, set the font size to `varFontSizeModern`.  
  → This ensures the text matches the default 13pt font size of classic controls.  
- When changing the font size of a **classic control**, set it to `varFontSizeClassic` and update the variable value in the App’s Formulas property.

---

## Conclusion

By standardizing font sizes with variables, you can ensure consistent and professional-looking text across both modern and classic controls in your canvas app.

**Happy Coding!**
