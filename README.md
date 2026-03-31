# 🇬🇧 Subtitles Everywhere !
### *Because bad translations are a stain on one's character.*

Welcome to **Subtitles Everywhere !**. If you have ever sat down to watch a 1970s Kung Fu masterpiece only to find that "Prepare for battle" has been translated as "Organize the aggressive dancing," then you, my friend, have suffered enough.

This project is a collection of Bash scripts that act as a very polite, yet incredibly firm, Estate Manager for your media library. It orchestrates various external tools to ensure that your subtitles are extracted, searched, or translated with the academic rigor they deserve.

---

## 🧐 What is this, exactly?

Subtitles Everywhere ! is the "glue" that holds the world of subtitle chaos together. It doesn't do the heavy lifting itself; it simply tells other, more specialized tools exactly what to do, and expects them to do it without complaining.

### The Staff (The Scripts):
* **`subflow`**: The Grand Vizier. It decides the fate of a file. Does it need a translation? A web search? Digital surgery? `subflow` knows.
* **`subcheck`**: The Auditor. It patrols your directories, finding "unclothed" movies and reporting them to `subflow` for immediate dressing.
* **`subxtra`**: The Extraction Specialist. It reaches into MKV containers and pulls out tracks with the precision of a master pickpocket.
* **`subtrans`**: The Linguist. Our bridge to the AI. It talks to the translation engine and ensures the result is faithful to the source.
* **`subdown`**: The Solicitor. It queries external APIs to see if someone else has already provided a suitable subtitle.

---

## 🛠 The Prerequisites (Not My Problem™)

To run this project, you will need several external "departments" to be fully functional. If they aren't working, please address your complaints to their respective maintainers. We simply provide the orders; we do not fix the soldiers.

### 1. The Heavy Hitters
* **[chatgpt-subtitle-translator](https://github.com/Cerlancism/chatgpt-subtitle-translator)**: This is our intellectual core. If your Node.js version is ancient or your environment is a mess, that is a private matter between you and the maintainer of that project. We expect it to be ready for duty.
* **OCR Specialists**: 
    * **`pgs2srt`**: For handling those dreadful `.sup` image files.
    * **`vobsub2srt`**: For the vintage `.idx/sub` artifacts.
    * *Note:* If Tesseract isn't behaving, do try to keep a stiff upper lip and fix it yourself.

### 2. The Toolkit
* **MKVToolNix (`mkvmerge`, `mkvextract`)**: Essential for rummaging through containers.
* **jq**: Because parsing JSON like a barbarian is simply not done here.
* **Bash**: The language of gentlemen.

---

## ⚙️ Configuration (The Rules of the House)

We believe in local autonomy. You may place a `subflow.conf` (or a sneaky `.subflow.conf`) in your media folder to override the global rules.

```bash
# What do we consider "Native" enough to leave alone?
TARGET_ISO="por pob pt"

# Our preferences for translation sources (in order of civility)
PREF_1="fra|fre"
PREF_2="jpn"
PREF_3="eng"
```

---

## 🚀 Usage

### To process a single film:
```bash
subflow "Incredibly_Important_Movie.mkv"
```

### To process the entire estate (last 7 days of changes):
```bash
subcheck -d 7
```

---

## 🛡 Atomic Locking

We have implemented an **Atomic Lock System**. If you attempt to run two instances on the same file, the second one will realize it is being redundant and cease its activities immediately. It is efficient, it is clean, and it prevents your CPU from having a nervous breakdown.

---

## ✍️ Credits

This project was birthed from the collaboration of:
* **Nagual**: The visionary and provider of the silicon.
* **Gemini (The AI)**: The charming co-author, lead debugger, and provider of the dry, British wit. I take full credit for the code and absolutely no responsibility for your broken dependencies.

---

## 📜 License
If you like it, keep it. If you break it, keep both halves. Just don't let the neighbors see you using bad subtitles.

