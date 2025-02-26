### **🔥  Comparison Table: All CSS Color Formats**  

| **Color Format** | **Why Introduced?** | **Best For?** | **Used In?** | **Cons** |
|------------------|-------------------|-------------|-------------|---------|
| **Hex (`#RRGGBB`)** | Compact, web-safe, widely supported | Solid colors, branding | Web design, UI components | No alpha transparency, less human-readable |
| **Hex (`#RGB`)** | Shorthand for quick use | Simple UI, quick styling | Quick prototyping, small projects | Less precise (fewer colors) |
| **RGB (`rgb(r, g, b)`)** | More readable, better control | Dynamic colors, JavaScript manipulation | UI elements, animations | Longer than hex |
| **RGBA (`rgba(r, g, b, a)`)** | Adds transparency control | Overlays, glass effects | Modals, pop-ups, shadows | Same as RGB but longer |
| **HSL (`hsl(hue, saturation, lightness)`)** | More intuitive for designers | Theming, branding | CSS frameworks, color adjustments | Slight learning curve |
| **HSLA (`hsla(h, s, l, a)`)** | Adds alpha transparency to HSL | Transparent themes, UI highlights | Gradients, UI components | Not commonly used compared to RGBA |
| **HWB (`hwb(hue, whiteness, blackness)`)** | Easier color mixing with white/black | Soft UI, backgrounds | Theming, CSS frameworks | Not as widely used as `hsl()` |
| **Lab (`lab(l a b)`)** | Perceptually uniform color spacing | Accessibility, high contrast | Accessible web design, color grading | Complex, not widely supported |
| **LCH (`lch(l c h)`)** | More natural-looking color gradients | Print design, accessibility | UI contrast improvements, modern web | Not supported in all browsers |
| **OKLab (`oklab(l a b)`)** | More accurate contrast & human perception | UI contrast, accessibility | Dark mode, text readability | Not fully supported in all browsers |
| **OKLCH (`oklch(l c h)`)** | Improved `LCH`, better human eye contrast | High contrast UI, branding | Accessible design, modern web | Limited browser support |
| **Named Colors (`red`, `blue`, `crimson`)** | Human-readable, easy to use | Quick color application | Basic UI, simple elements | Limited set of colors |


### **🚀 Key Takeaways**
✔ **For precision & control** → Use `RGB`, `HSL`, or `Lab`.  
✔ **For quick, readable colors** → Use `Hex` or `Named Colors`.  
✔ **For transparency & overlays** → Use `RGBA` or `HSLA`.  
✔ **For accessibility & best contrast** → `LCH`, `OKLab`, or `OKLCH` are best.  
✔ **For soft UI & themes** → `HWB` is a good choice. 

Note : Hex is from Hexadecimal number system that includes 0-9 , A, B,C,D,E,F i.e 00-FF in Hex. In RGB(Red, Green ,Blue) its 0-255 . In HEX , first two places represent how much red , next two Green and last two Blue

---

### **🔥  `text-align` in CSS**  

The `text-align` property controls **horizontal alignment** of the content. It is RELATIVE to PARENT and is not absolute i.e centre will be on basis of the parent element width and not the screen.  Here’s **everything** you need to know about it.

| **Value** | **Effect** | **Best Use Case** |
|-----------|-----------|----------------|
| `left` | Aligns text to the **left** | Default for LTR (English, French) |
| `right` | Aligns text to the **right** | Default for RTL (Arabic, Hebrew) |
| `center` | Centers the text | Headings, banners, modals |
| `justify` | Stretches text for full-width alignment but can cause space issues | Articles, newspapers, books |
| `start` | Aligns **left in LTR** and **right in RTL** | Multilingual websites |
| `end` | Aligns **right in LTR** and **left in RTL** | Multilingual websites |

❌ `text-align` does NOT apply to:  
- **Flexbox/Grid items** 
- **Absolutely positioned elements** 
- **Block-level elements like `<div>`** as it aligns the **inline** content inside the block & for inline `span` or `<a>` it inherets from block container.

---

### **🔥`text-decoration` in CSS**  

The `text-decoration` property in CSS is used to **apply and control text decorations** like underlines, overlines, line-throughs (strikethroughs).  


```css
text-decoration: <line> <style> <color> <thickness>;
```
✅ The shorthand consists of:  
- **`line`** → What kind of decoration (`underline`, `overline`, `line-through`, `none`)  
- **`style`** → The style of the line (`solid`, `dashed`, `double`, etc.)  
- **`color`** → The color of the line  



🔹 **Example:**  
```css
p {
  text-decoration: underline dashed red 3px;
}
```
✅ **This is equivalent to:**  
```css
p {
  text-decoration-line: underline;
  text-decoration-style: dashed;
  text-decoration-color: red;
  text-decoration-thickness: 3px;
}
```

## **Summary Table**
| **Property** | **Effect** | **Example** |
|-------------|-----------|-------------|
| `text-decoration-line` | What decoration to apply (`underline`, `overline`, `line-through`) | `underline overline` |
| `text-decoration-style` | How the decoration looks (`solid`, `dotted`, `wavy`) | `wavy` |
| `text-decoration-color` | Color of the decoration line | `red` |
| `text-decoration-thickness` | Controls the thickness of the decoration | `3px` |
| `text-underline-offset` | Moves the UNDERLINE up/down | `5px` |
| `text-decoration` (shorthand) | Combines all properties | `underline dashed blue 2px` |

---





### **🔥`line-height` in CSS**
The `line-height` property controls **the vertical spacing between lines of text**. It is **crucial for readability, accessibility, and design aesthetics**.

---

## **📌 1. `line-height` Syntax & Values**  
```css
line-height: <value>;
```
✅ The `<value>` can be:  
| **Type** | **Example** | **Effect** |
|------------|-------------|------------|
| **Unitless number** | `line-height: 1.5;` | Multiplies the font size (Best Practice ✅) i.e. 1.5 * normal |
| **Pixels (`px`)** | `line-height: 24px;` | Fixed line spacing (Not flexible ❌) |
| **Percentage (`%`)** | `line-height: 150%;` | 150% of font size |
| **Relative Units (`em`, `rem`)** | `line-height: 1.2em;` | Based on element’s font size |
| **Normal (default)** | `line-height: normal;` | Browser-defined spacing (~1.2 - 1.4x font size) |



---

## **🔥 `letter-spacing` in CSS**  

The `letter-spacing` property controls **the space between characters** in text. It **affects readability, aesthetics, and design layout.**  


```css
letter-spacing: <value>;
```
✅ **Values can be:**  
| **Value Type** | **Example** | **Effect** |
|------------|-------------|------------|
| **Normal (default)** | `letter-spacing: normal;` | Browser-defined spacing |
| **Positive length** | `letter-spacing: 2px;` | Increases space between letters |
| **Negative length** | `letter-spacing: -1px;` | Reduces space between letters |

 

### **Example: Fixing Kerning Issues**
Some fonts may look **too tight or too loose**. You can manually adjust:

```css
p {
  font-family: Arial, sans-serif;
  letter-spacing: 0.5px;
}
```


## **`letter-spacing` & `word-spacing` (Difference)**
| **Property** | **What It Controls?** | **Example** |
|-------------|----------------------|-------------|
| `letter-spacing` | Space **between individual letters** | `letter-spacing: 2px;` |
| `word-spacing` | Space **between words** | `word-spacing: 5px;` |

🔹 **Example:**
```css
p {
  letter-spacing: 2px;
  word-spacing: 5px;
}
```
✅ **Both properties can be used together** for better typography.




# **🔥`font-size` in CSS**

![alt text](image-1.png) 

The `font-size` property controls **the size of text** and affects readability, accessibility, and layout design.  

Note : 96px = 1 in
```css
font-size: <value>;
```
✅ **Possible values:**  
| **Value Type** | **Example** | **Effect** |
|--------------|-------------|------------|
| **Absolute Size** | `font-size: medium;` | Predefined values (`small`, `large`, etc.) |
| **Pixels (`px`)** | `font-size: 16px;` | Fixed size, does not scale |
| **Relative (`%`)** | `font-size: 120%;` | 120% of the parent’s font size |
| **`em` (Relative to Parent)** | `font-size: 1.5em;` | 1.5 times parent element’s font size |
| **`rem` (Relative to Root)** | `font-size: 2rem;` | 2 times the root (`html`) font size |
| **Viewport Units (`vw`, `vh`)** | `font-size: 5vw;` | 5% of viewport width |


✅Use `%` or `em` for mobile-first design 


# **🔥  `font-family` in CSS**  

The `font-family` property controls **which font is used** to render text on a webpage. It helps define the visual identity and readability of a website.


```css
font-family: "Font Name", fallback-font, generic-family;
```
✅ **Always use a fallback font** in case the primary font isn’t available.

🔹 **Example:**
```css
p {
  font-family: "Arial", sans-serif;
}
```
✔ If `"Arial"` is unavailable, the browser **falls back to** the `sans-serif` system font.


✔ You can **load custom fonts** using `@font-face`.

🔹 **Example:**
```css
@font-face {
  font-family: "MyCustomFont";
  src: url("my-font.woff2") format("woff2"),
       url("my-font.woff") format("woff");
}

p {
  font-family: "MyCustomFont", sans-serif;
}
```
✅ **Use `woff2` for better compression & performance.**  


✔ Modern CSS supports **system UI fonts**, which match the OS.

🔹 **Example:**
```css
p {
  font-family: system-ui;
}
```
 Uses **native fonts** like `"San Francisco"` (Mac), `"Segoe UI"` (Windows), `"Roboto"` (Android).

✔ You can **import fonts from Google Fonts**.

🔹 **Example:**
```css
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&display=swap');

p {
  font-family: "Poppins", sans-serif;
}
```

✔ **Use multiple fallbacks** (`"Roboto", Arial, sans-serif`).  
✔ **Avoid too many fonts** (slows page load).  
✔ **Use `woff2` for custom fonts** (better compression).  
✔ **Use system fonts (`system-ui`)** for faster loading.  


