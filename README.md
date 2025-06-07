# 🚀 FlutterSheet for React

A vanilla bottom flutter sheet component for React, Great for settings, menus, and interactive overlays.

---

## 📦 Features

- ✨ Clean & customizable design
- 🎯 Drag to dismiss
- 📱 Mobile-first UX (Back button support)
- 🧾 Simple API: `<FlutterSheet>` with `open`, `setOpen`, and optional styling

---

## 📸 Preview

![FlutterSheet Preview](https://raw.githubusercontent.com/aerxeo/React-FlutterSheet-Vanilla-/refs/heads/main/preview.gif) 

---

## 🚀 Usage

### 1. Installation

Just copy or download `FlutterSheet.js` into your project or create a component file:

```tree
your-project/
├── components/
│   └── FlutterSheet.js
```


---

2. Usage example

```js
import React, { useState } from 'react';
import FlutterSheet from './FlutterSheet';

function App() {
  const [isFlutterSheetOpen, setisFlutterSheetOpen] = useState(false);

  return (
    <div>
      <button onClick={() => setisFlutterSheetOpen(!isFlutterSheetOpen)}>Open Sheet</button>

      <FlutterSheet height={"100dvh"} style={{ background: '#fff' }} animation={100} backdrop={0.5} open={isFlutterSheetOpen} setOpen={setisFlutterSheetOpen} >
        <FlutterSheet.title style={{ color: '#000' }}>Hello world!</FlutterSheet.title>
        <FlutterSheet.content style={{ padding: '16px' }}>
        
          <div style={{height:"500vh", width:"100%", background:"#ddd"}}>A loooooooooooooooooooong div to test scroll</div>
          
        </FlutterSheet.content>
      </FlutterSheet>
    </div>
  );
}

export default App;
```
---
🧱 Subcomponents

<FlutterSheet.title>

Displays a centered heading + line separator.

<FlutterSheet.title style={{ color: '#000' }}>Settings</FlutterSheet.title>


---

<FlutterSheet.content>

Wraps scrollable content inside the sheet. Automatically handles scroll + drag.

<FlutterSheet.content style={{ padding: '1rem' }}>
  {/* your content */}
</FlutterSheet.content>

---

🔍 Props Explained

>height:
>Type: string (like "90dvh" or "400px")
>Default: Auto height based on content
>Use it when: You want to limit or expand the sheet's height.
> If you don’t define height, the sheet will size itself based on the content automatically.

---

>animation
>Type: number (milliseconds)
>Default: 180
>Use it for: How fast the sheet opens/closes.

---

>backdrop
>Type: number (from 0 to 1)
>Default: 0.3
>Use it for: How dark the background overlay is when the sheet is open.

---

>open
>Type: boolean
>Use it for: Telling the sheet if it should be visible or not.

---

>setOpen
>Type: function
>Use it for: Closing the sheet (e.g. on drag down or backdrop click).

---


📋 Notes

Drag to dismiss works on both touch and mouse

The sheet adds/removes overflow: hidden on the body to prevent background scrolling

The browser back button closes the sheet when open


###That's it! Just plug in what you need and it works ✨

---

📄 License

MIT — free for personal and commercial use.

---

💡 Credits

Created by ```@erxeo``` 
Inspired on Instagram's modal
