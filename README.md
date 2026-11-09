# Clipperdirac

Lambi video se viral short clips banane wala Android app (Kotlin). Sab kuch phone pe chalta hai.

**Kya karta hai**
1. Video chuno -> offline speech-to-text (Vosk, word-by-word timing)
2. AI (Gemini key 1, Gemini key 2, Grok) poori video me se best moments chunta hai
   - Keys baari-baari use hoti hain; ek ki limit lage to agli par chala jata hai
   - Lambi video 12-minute ke parts me tut ke alag-alag key se analyze hoti hai
3. Edit: pauses / umm / hmm / faltu hissa kat jata hai, 9:16 crop, har cut pe zoom punch-in,
   bade word-by-word captions (bolne wala shabd yellow), whoosh SFX, optional background music
4. Har video ka alag folder: `Movies/Clipperdirac/<video>_<time>/` (Gallery me dikhta hai)

## GitHub se APK banana (laptop ki zarurat nahi)
1. GitHub pe naya repo `clipperdirac` banao.
2. Is project ki saari files repo me daalo (folder structure same rehna chahiye, `.github/workflows/build.yml` bhi).
3. `main` branch pe push hote hi **Actions** tab me build chalega (~5-8 min).
4. Build poora hone par repo ke **Releases** me `Clipperdirac.apk` milega. Download karke install karo
   (Settings me "Install unknown apps" allow karna padega).
5. Build fail ho to Actions > us run > failed step ka log copy karke mujhe bhejo, main fix kar dunga.

## Keys kahan se
- Gemini: https://aistudio.google.com/apikey (free)
- Grok: https://console.x.ai

## Dhyan rakhne wali baatein
- Pehli baar speech model (~40MB) download hota hai, phir offline.
- Transcription phone ki speed pe depend karti hai: 30 min ki video me kuch minute lag sakte hain. Processing ke time app band mat karo.
- Vosk ka small model free aur offline hai par Whisper jitna accurate nahi; shor wali ya mixed-language video me captions me galtiyan aa sakti hain.
- Hinglish ke liye "Hindi" chuno (captions Devanagari me aayenge).
- 
