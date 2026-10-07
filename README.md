### DetectFontsinPSD

Easily identify all the fonts used in a Photoshop file.

A Photoshop ExtendScript that lists every font actually used in the open document, including
fonts inside text layers you would otherwise have to click through one at a time. It walks the
document's layer list via the Action Manager, pulls the PostScript name from each text style
range, de-duplicates, sorts, and shows the result in a single dialog.

Useful when you inherit a PSD and need to know what to license, install, or substitute before
you can open it cleanly.

## Install

Copy `detectfonts.jsx` into the Photoshop scripts folder:

| Platform | Path |
|---|---|
| macOS | `/Applications/Adobe Photoshop <version>/Presets/Scripts/` |
| Windows | `C:\Program Files\Adobe\Adobe Photoshop <version>\Presets\Scripts\` |

Restart Photoshop. The script then appears under **File > Scripts > detectfonts**.

To run it without installing, use **File > Scripts > Browse…** and pick the `.jsx` directly.

## Use

Open a PSD and run the script. It reports the number of fonts found and lists their PostScript
names, one per line. With no document open, or a document with no text layers, it says so
instead.

## Notes

- Reports PostScript names (e.g. `HelveticaNeue-Bold`), which is what the file actually
  references -- not the friendly family/style pair shown in the character panel.
- Reads only the open document; it does not scan a folder of PSDs.
- Action Manager based, so it works on documents whose text layers are locked or hidden.
