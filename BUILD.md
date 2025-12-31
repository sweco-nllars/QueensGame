# 🔨 APK Build Instructies

Dit document beschrijft hoe je een Android APK kunt bouwen van de Queens Puzzel app.

## Methode 1: PWABuilder (Makkelijkst)

Geen lokale installatie nodig!

1. **De app is al gehost op GitHub Pages:**
   ```
   https://sweco-nllars.github.io/QueensGame/
   ```

2. **Ga naar [PWABuilder.com](https://www.pwabuilder.com/)**

3. **Voer de URL in** en klik "Start"

4. **Download Android APK**
   - Kies "Android"
   - Selecteer "APK" of "Android App Bundle"
   - Download

## Methode 2: Capacitor (Lokaal)

### Vereisten

- Node.js 16+ ([Download](https://nodejs.org/))
- Java JDK 11+ ([Download](https://adoptium.net/))
- Android Studio ([Download](https://developer.android.com/studio))

### Stappen

```bash
# 1. Clone repository
git clone https://github.com/sweco-nllars/QueensGame.git
cd QueensGame

# 2. Installeer dependencies
npm init -y
npm install @capacitor/core @capacitor/cli @capacitor/android

# 3. Maak www directory
mkdir -p www
cp index.html www/
cp manifest.json www/
cp -r icons www/

# 4. Initialiseer Capacitor
npx cap init "Queens Puzzel" "com.queenspuzzel.app" --web-dir www

# 5. Voeg Android platform toe
npx cap add android

# 6. Sync project
npx cap sync android

# 7. Open in Android Studio (optioneel)
npx cap open android

# 8. Bouw APK via command line
cd android
./gradlew assembleDebug
```

De APK staat in: `android/app/build/outputs/apk/debug/app-debug.apk`

## Methode 3: Android Studio

1. Volg stappen 1-6 van Methode 2
2. Open project in Android Studio:
   ```bash
   npx cap open android
   ```
3. Menu: `Build` → `Build Bundle(s) / APK(s)` → `Build APK(s)`
4. Klik "locate" in de popup

## APK Installeren

### Via ADB
```bash
adb install app-debug.apk
```

### Handmatig
1. Kopieer APK naar telefoon
2. Open bestandsbeheer
3. Tik op APK
4. Sta "Onbekende bronnen" toe
5. Installeer

## Signed Release APK

Voor Play Store publicatie:

```bash
# Genereer keystore (eenmalig)
keytool -genkey -v -keystore queens-release.keystore \
  -alias queens -keyalg RSA -keysize 2048 -validity 10000

# Bouw release
cd android
./gradlew assembleRelease
```

## Problemen Oplossen

### JAVA_HOME niet gevonden
```bash
export JAVA_HOME=/usr/lib/jvm/java-11-openjdk
```

### ANDROID_HOME niet gevonden
```bash
export ANDROID_HOME=$HOME/Android/Sdk
export PATH=$PATH:$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools
```

### SDK niet gevonden
Maak `android/local.properties`:
```
sdk.dir=/pad/naar/Android/Sdk
```
