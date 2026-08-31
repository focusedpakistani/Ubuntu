<p align="center">
  <img src="https://img.shields.io/badge/Ubuntu%20on%20Android-E95420?style=for-the-badge&logo=ubuntu&logoColor=white" alt="Ubuntu on Android"/>
  <img src="https://img.shields.io/badge/Termux-000000?style=for-the-badge&logo=android&logoColor=white" alt="Termux"/>
  <img src="https://img.shields.io/badge/Rootless-00C853?style=for-the-badge&logo=shield&logoColor=white" alt="Rootless"/>
</p>

<h1 align="center">🐧 UBUNTU on Android</h1>

<p align="center">
  <b>Run a full Ubuntu Desktop (XFCE / GNOME) directly on your Android device using Termux & Udroid.</b>
</p>

<p align="center">
  <a href="#english">🇺🇸 English</a> •
  <a href="#urdu">🇵🇰 اردو</a> •
  <a href="#chinese">🇨🇳 中文</a> •
  <a href="#korean">🇰🇷 한국어</a> •
  <a href="#french">🇫🇷 Français</a> •
  <a href="#hindi">🇮🇳 हिन्दी</a> •
  <a href="#arabic">🇸🇦 العربية</a> •
  <a href="#spanish">🇪🇸 Español</a> •
  <a href="#dutch">🇳🇱 Nederlands</a> •
  <a href="#indonesian">🇮🇩 Bahasa Indonesia</a> •
  <a href="#german">🇩🇪 Deutsch</a> •
  <a href="#portuguese">🇧🇷 Português</a> •
  <a href="#russian">🇷🇺 Русский</a> •
  <a href="#japanese">🇯🇵 日本語</a> •
  <a href="#turkish">🇹🇷 Türkçe</a>
</p>

---

## 📋 System Requirements | متطلبات النظام | 系统要求

| Requirement | Minimum | Recommended |
|-------------|---------|-------------|
| **Internet Data** | 3 GB | 4 GB+ (stable connection) |
| **Storage** | 6 GB free | 10 GB+ free |
| **RAM** | 4 GB | 8 GB+ |
| **Android** | 7.0+ | 10+ |

> ⚠️ **Note:** The installation command downloads all core dependencies including X11 display servers and audio drivers. A stable Wi-Fi connection is strongly recommended.

---

## ⬇️ Prerequisites | المتطلبات الأساسية | 先决条件

Before running any commands, install these two apps on your Android device:

| App | Download Link |
|-----|---------------|
| **Termux** | [F-Droid](https://f-droid.org/en/packages/com.termux/) |
| **Termux-X11** | [GitHub Nightly](https://github.com/termux/termux-x11/releases/tag/nightly) |

> 💡 **Pro Tip:** Install [Unexpected Keyboard](https://github.com/Julow/Unexpected-Keyboard) for a much better desktop browsing & app experience inside Ubuntu.

---

<a id="english"></a>
## 🇺🇸 English

### 🚀 One-Line Installation
Run this **single command** inside Termux. It installs everything automatically:

```bash
pkg update -y && pkg upgrade -y && pkg install x11-repo -y && pkg install termux-x11-nightly -y && . <(curl -Ls https://bit.ly/udroid-installer) && udroid install jammy:xfce4
```

- ⏱️ Time: 30 minutes (depends on your internet speed)
- 📶 Internet: Required — at least 4 GB data recommended
- 🔋 Tip: Keep your device plugged in during installation

▶️ Launch Ubuntu

Run these commands one by one inside Termux:

```bash
# 1. Start the X11 display server in background
termux-x11 :1 -ac &
```

```bash
# 2. Login to Ubuntu
udroid login jammy:xfce4
```

```bash
# 3. Set the display environment
export DISPLAY=:1
```

```bash
# 4. Start the XFCE4 desktop
startxfce4 &
```

> 🖥️ Important: Make sure Termux-X11 app is open in the background before running the last command. After `startxfce4 &` executes, switch to the Termux-X11 app to see your Ubuntu desktop!

🌟 Features
- Zero-Touch Configuration — All core dependencies, X11 servers & audio drivers installed in one go
- Smart Auto-Fix — Automatically resolves `Access Denied`, `Display Locked`, and common permission errors
- Full Native Audio — Integrated PulseAudio support (fixes audio in Firefox, VLC, etc.)
- 100% Rootless — No root access required, keeping your device secure

---

🇵🇰 اردو (Urdu)

🚀 ایک لائن میں انسٹالیشن
یہ ایک کمانڈ Termux میں چلائیں۔ یہ سب کچھ خودکار انسٹال کر دے گی:

```bash
pkg update -y && pkg upgrade -y && pkg install x11-repo -y && pkg install termux-x11-nightly -y && . <(curl -Ls https://bit.ly/udroid-installer) && udroid install jammy:xfce4
```

- ⏱️ وقت: تقریباً 30 منٹ (آپ کی انٹرنیٹ سپیڈ پر منحصر ہے)
- 📶 انٹرنیٹ: ضروری — کم از کم 4 GB ڈیٹا تجویز کردہ
- 🔋 نکتہ: انسٹالیشن کے دوران اپنے فون کو چارج پر رکھیں

▶️ Ubuntu چلائیں

یہ کمانڈز Termux میں ایک ایک کرکے چلائیں:

```bash
# 1. X11 ڈسپلے سرور بیک گراؤنڈ میں شروع کریں
termux-x11 :1 -ac &
```

```bash
# 2. Ubuntu میں لاگ ان کریں
udroid login jammy:xfce4
```

```bash
# 3. ڈسپلے ماحول سیٹ کریں
export DISPLAY=:1
```

```bash
# 4. XFCE4 ڈیسک ٹاپ شروع کریں
startxfce4 &
```

> 🖥️ اہم: آخری کمانڈ چلانے سے پہلے یقینی بنائیں کہ Termux-X11 ایپ بیک گراؤنڈ میں کھلی ہو۔ `startxfce4 &` چلانے کے بعد Termux-X11 ایپ پر جائیں اور Ubuntu ڈیسک ٹاپ کا لطف اٹھائیں!

🌟 خصوصیات
- زیرو ٹچ کنفیگریشن — تمام بنیادی انحصار، X11 سرورز اور آڈیو ڈرائیورز ایک ہی بار میں
- اسمارٹ آٹو فکس — `Access Denied`، `Display Locked` اور عام پرمیشن ایررز خودکار حل
- مکمل نیٹو آڈیو — PulseAudio انٹیگریشن (Firefox، VLC وغیرہ میں آڈیو ٹھیک کرتا ہے)
- 100% روٹ لیس — روٹ رسائی کی ضرورت نہیں، آپ کا ڈیوائس محفوظ رہتا ہے

---

🇨🇳 中文 (Chinese)

🚀 一键安装
在 Termux 中运行以下单行命令，自动安装所有内容：

```bash
pkg update -y && pkg upgrade -y && pkg install x11-repo -y && pkg install termux-x11-nightly -y && . <(curl -Ls https://bit.ly/udroid-installer) && udroid install jammy:xfce4
```

- ⏱️ 时间： 约 30 分钟（取决于网速）
- 📶 网络： 必需 — 建议至少 4 GB 流量
- 🔋 提示： 安装期间请保持设备充电

▶️ 启动 Ubuntu

在 Termux 中依次运行以下命令：

```bash
# 1. 在后台启动 X11 显示服务器
termux-x11 :1 -ac &
```

```bash
# 2. 登录 Ubuntu
udroid login jammy:xfce4
```

```bash
# 3. 设置显示环境变量
export DISPLAY=:1
```

```bash
# 4. 启动 XFCE4 桌面
startxfce4 &
```

> 🖥️ 重要： 运行最后一条命令前，请确保 Termux-X11 应用已在后台打开。执行 `startxfce4 &` 后，切换到 Termux-X11 应用即可看到 Ubuntu 桌面！

🌟 功能特性
- 零接触配置 — 一次性安装所有核心依赖、X11 服务器和音频驱动
- 智能自动修复 — 自动解决 `Access Denied`、`Display Locked` 等常见错误
- 完整原生音频 — 集成 PulseAudio（修复 Firefox、VLC 等音频问题）
- 100% 免 Root — 无需 Root 权限，保障设备安全

---

🇰🇷 한국어 (Korean)

🚀 원클릭 설치
Termux에서 다음 단일 명령어를 실행하면 모든 것이 자동으로 설치됩니다:

```bash
pkg update -y && pkg upgrade -y && pkg install x11-repo -y && pkg install termux-x11-nightly -y && . <(curl -Ls https://bit.ly/udroid-installer) && udroid install jammy:xfce4
```

- ⏱️ 소요 시간: 약 30분 (인터넷 속도에 따라 다름)
- 📶 인터넷: 필수 — 최소 4 GB 데이터 권장
- 🔋 팁: 설치 중 기기를 충전 상태로 유지하세요

▶️ Ubuntu 실행

Termux에서 다음 명령어를 하나씩 실행하세요:

```bash
# 1. 백그라운드에서 X11 디스플레이 서버 시작
termux-x11 :1 -ac &
```

```bash
# 2. Ubuntu에 로그인
udroid login jammy:xfce4
```

```bash
# 3. 디스플레이 환경 변수 설정
export DISPLAY=:1
```

```bash
# 4. XFCE4 데스크톱 시작
startxfce4 &
```

> 🖥️ 중요: 마지막 명령어 실행 전 Termux-X11 앱이 백그라운드에서 실행 중인지 확인하세요. `startxfce4 &` 실행 후 Termux-X11 앱으로 전환하면 Ubuntu 데스크톱이 보입니다!

🌟 주요 기능
- 제로 터치 구성 — 핵심 의존성, X11 서버 및 오디오 드라이버를 한 번에 설치
- 스마트 자동 수정 — `Access Denied`, `Display Locked` 및 일반적인 권한 오류 자동 해결
- 완전한 네이티브 오디오 — PulseAudio 통합 (Firefox, VLC 등에서 오디오 문제 해결)
- 100% 루트 불필요 — 루트 권한 없이 기기 보안 유지

---

🇫🇷 Français (French)

🚀 Installation en une ligne
Exécutez cette commande unique dans Termux. Tout s'installera automatiquement :

```bash
pkg update -y && pkg upgrade -y && pkg install x11-repo -y && pkg install termux-x11-nightly -y && . <(curl -Ls https://bit.ly/udroid-installer) && udroid install jammy:xfce4
```

- ⏱️ Durée : 30 minutes (selon votre vitesse internet)
- 📶 Internet : Requis — au moins 4 Go de données recommandés
- 🔋 Conseil : Gardez votre appareil branché pendant l'installation

▶️ Lancer Ubuntu

Exécutez ces commandes une par une dans Termux :

```bash
# 1. Démarrer le serveur d'affichage X11 en arrière-plan
termux-x11 :1 -ac &
```

```bash
# 2. Se connecter à Ubuntu
udroid login jammy:xfce4
```

```bash
# 3. Définir la variable d'environnement d'affichage
export DISPLAY=:1
```

```bash
# 4. Démarrer le bureau XFCE4
startxfce4 &
```

> 🖥️ Important : Assurez-vous que l'application Termux-X11 est ouverte en arrière-plan avant d'exécuter la dernière commande. Après `startxfce4 &`, basculez vers l'application Termux-X11 pour voir votre bureau Ubuntu !

🌟 Fonctionnalités
- Configuration Zero-Touch — Installe toutes les dépendances, serveurs X11 et pilotes audio en une seule fois
- Correction automatique intelligente — Résout automatiquement `Access Denied`, `Display Locked` et les erreurs de permission courantes
- Audio natif complet — Support PulseAudio intégré (corrige l'audio dans Firefox, VLC, etc.)
- 100% Sans Root — Aucun accès root requis, votre appareil reste sécurisé

---

🇮🇳 हिन्दी (Hindi)

🚀 एक लाइन में इंस्टॉलेशन
Termux में यह एक कमांड चलाएं। यह सब कुछ स्वचालित रूप से इंस्टॉल कर देगी:

```bash
pkg update -y && pkg upgrade -y && pkg install x11-repo -y && pkg install termux-x11-nightly -y && . <(curl -Ls https://bit.ly/udroid-installer) && udroid install jammy:xfce4
```

- ⏱️ समय: लगभग 30 मिनट (आपकी इंटरनेट स्पीड पर निर्भर)
- 📶 इंटरनेट: आवश्यक — कम से कम 4 GB डेटा अनुशंसित
- 🔋 सुझाव: इंस्टॉलेशन के दौरान अपने डिवाइस को चार्ज पर रखें

▶️ Ubuntu चलाएं

Termux में ये कमांड्स एक-एक करके चलाएं:

```bash
# 1. बैकग्राउंड में X11 डिस्प्ले सर्वर शुरू करें
termux-x11 :1 -ac &
```

```bash
# 2. Ubuntu में लॉग इन करें
udroid login jammy:xfce4
```

```bash
# 3. डिस्प्ले एनवायरनमेंट सेट करें
export DISPLAY=:1
```

```bash
# 4. XFCE4 डेस्कटॉप शुरू करें
startxfce4 &
```

> 🖥️ महत्वपूर्ण: अंतिम कमांड चलाने से पहले सुनिश्चित करें कि Termux-X11 ऐप बैकग्राउंड में खुला हो। `startxfce4 &` चलाने के बाद Termux-X11 ऐप पर जाएं और Ubuntu डेस्कटॉप का आनंद लें!

🌟 विशेषताएं
- जीरो-टच कॉन्फ़िगरेशन — सभी कोर निर्भरताएं, X11 सर्वर और ऑडियो ड्राइवर एक साथ
- स्मार्ट ऑटो-फिक्स — `Access Denied`, `Display Locked` और सामान्य अनुमति त्रुटियां स्वचालित रूप से ठीक
- पूर्ण नेटिव ऑडियो — PulseAudio एकीकरण (Firefox, VLC आदि में ऑडियो ठीक करता है)
- 100% रूटलेस — रूट एक्सेस की आवश्यकता नहीं, आपका डिवाइस सुरक्षित रहता है

---

🇸🇦 العربية (Arabic)

🚀 التثبيت بسطر واحد
شغّل هذا الأمر الواحد داخل Termux. سيتم تثبيت كل شيء تلقائيًا:

```bash
pkg update -y && pkg upgrade -y && pkg install x11-repo -y && pkg install termux-x11-nightly -y && . <(curl -Ls https://bit.ly/udroid-installer) && udroid install jammy:xfce4
```

- ⏱️ المدة: حوالي 30 دقيقة (تعتمد على سرعة الإنترنت)
- 📶 الإنترنت: مطلوب — يُنصح بـ 4 جيجابايت على الأقل
- 🔋 نصيحة: أبقِ جهازك موصولاً بالشاحن أثناء التثبيت

▶️ تشغيل Ubuntu

شغّل هذه الأوامر واحدًا تلو الآخر داخل Termux:

```bash
# 1. تشغيل خادم العرض X11 في الخلفية
termux-x11 :1 -ac &
```

```bash
# 2. تسجيل الدخول إلى Ubuntu
udroid login jammy:xfce4
```

```bash
# 3. تعيين متغير بيئة العرض
export DISPLAY=:1
```

```bash
# 4. تشغيل سطح المكتب XFCE4
startxfce4 &
```

> 🖥️ مهم: تأكد من أن تطبيق Termux-X11 مفتوح في الخلفية قبل تشغيل الأمر الأخير. بعد تنفيذ `startxfce4 &`، انتقل إلى تطبيق Termux-X11 لمشاهدة سطح مكتب Ubuntu!

🌟 الميزات
- إعداد بدون لمس — تثبيت جميع التبعيات الأساسية وخوادم X11 وبرامج تشغيل الصوت دفعة واحدة
- إصلاح ذكي تلقائي — يحل تلقائيًا أخطاء `Access Denied` و`Display Locked` وأخطاء الأذونات الشائعة
- صوت أصلي كامل — دعم PulseAudio مدمج (يصلح الصوت في Firefox وVLC وغيرهما)
- 100% بدون روت — لا يحتاج إلى صلاحيات الروت، جهازك يبقى آمناً

---

🇪🇸 Español (Spanish)

🚀 Instalación en una línea
Ejecuta este comando único dentro de Termux. Todo se instalará automáticamente:

```bash
pkg update -y && pkg upgrade -y && pkg install x11-repo -y && pkg install termux-x11-nightly -y && . <(curl -Ls https://bit.ly/udroid-installer) && udroid install jammy:xfce4
```

- ⏱️ Tiempo: 30 minutos (depende de tu velocidad de internet)
- 📶 Internet: Requerido — se recomiendan al menos 4 GB de datos
- 🔋 Consejo: Mantén tu dispositivo conectado durante la instalación

▶️ Iniciar Ubuntu

Ejecuta estos comandos uno por uno dentro de Termux:

```bash
# 1. Iniciar el servidor de pantalla X11 en segundo plano
termux-x11 :1 -ac &
```

```bash
# 2. Iniciar sesión en Ubuntu
udroid login jammy:xfce4
```

```bash
# 3. Establecer la variable de entorno de pantalla
export DISPLAY=:1
```

```bash
# 4. Iniciar el escritorio XFCE4
startxfce4 &
```

> 🖥️ Importante: Asegúrate de que la aplicación Termux-X11 esté abierta en segundo plano antes de ejecutar el último comando. ¡Después de `startxfce4 &`, cambia a la aplicación Termux-X11 para ver tu escritorio Ubuntu!

🌟 Características
- Configuración Zero-Touch — Instala todas las dependencias, servidores X11 y controladores de audio de una vez
- Corrección automática inteligente — Resuelve automáticamente `Access Denied`, `Display Locked` y errores de permiso comunes
- Audio nativo completo — Soporte PulseAudio integrado (corrige el audio en Firefox, VLC, etc.)
- 100% Sin Root — No se requiere acceso root, tu dispositivo permanece seguro

---

🇳🇱 Nederlands (Dutch)

🚀 Installatie in één regel
Voer dit ene commando uit in Termux. Alles wordt automatisch geïnstalleerd:

```bash
pkg update -y && pkg upgrade -y && pkg install x11-repo -y && pkg install termux-x11-nightly -y && . <(curl -Ls https://bit.ly/udroid-installer) && udroid install jammy:xfce4
```

- ⏱️ Tijd: 30 minuten (afhankelijk van je internetsnelheid)
- 📶 Internet: Vereist — minstens 4 GB data aanbevolen
- 🔋 Tip: Houd je apparaat aangesloten tijdens de installatie

▶️ Ubuntu starten

Voer deze commando's één voor één uit in Termux:

```bash
# 1. Start de X11 display server op de achtergrond
termux-x11 :1 -ac &
```

```bash
# 2. Log in op Ubuntu
udroid login jammy:xfce4
```

```bash
# 3. Stel de display omgevingsvariabele in
export DISPLAY=:1
```

```bash
# 4. Start het XFCE4 bureaublad
startxfce4 &
```

> 🖥️ Belangrijk: Zorg ervoor dat de Termux-X11 app op de achtergrond open is voordat je het laatste commando uitvoert. Na `startxfce4 &`, schakel over naar de Termux-X11 app om je Ubuntu bureaublad te zien!

🌟 Functies
- Zero-Touch Configuratie — Installeert alle kernafhankelijkheden, X11 servers en audiostuurprogramma's in één keer
- Slim Auto-Fix Systeem — Lost automatisch `Access Denied`, `Display Locked` en veelvoorkomende permissiefouten op
- Volledige Native Audio — Geïntegreerde PulseAudio ondersteuning (lost audio-problemen op in Firefox, VLC, etc.)
- 100% Rootloos — Geen root-toegang vereist, uw apparaat blijft veilig

---

🇮🇩 Bahasa Indonesia (Indonesian)

🚀 Instalasi Satu Baris
Jalankan perintah tunggal ini di dalam Termux. Semuanya akan terinstal secara otomatis:

```bash
pkg update -y && pkg upgrade -y && pkg install x11-repo -y && pkg install termux-x11-nightly -y && . <(curl -Ls https://bit.ly/udroid-installer) && udroid install jammy:xfce4
```

- ⏱️ Waktu: 30 menit (tergantung kecepatan internet Anda)
- 📶 Internet: Diperlukan — disarankan minimal 4 GB data
- 🔋 Tips: Pastikan perangkat Anda tetap terisi daya selama instalasi

▶️ Menjalankan Ubuntu

Jalankan perintah-perintah ini satu per satu di dalam Termux:

```bash
# 1. Mulai server tampilan X11 di latar belakang
termux-x11 :1 -ac &
```

```bash
# 2. Masuk ke Ubuntu
udroid login jammy:xfce4
```

```bash
# 3. Atur variabel lingkungan tampilan
export DISPLAY=:1
```

```bash
# 4. Mulai desktop XFCE4
startxfce4 &
```

> 🖥️ Penting: Pastikan aplikasi Termux-X11 terbuka di latar belakang sebelum menjalankan perintah terakhir. Setelah `startxfce4 &` dijalankan, beralihlah ke aplikasi Termux-X11 untuk melihat desktop Ubuntu Anda!

🌟 Fitur
- Konfigurasi Zero-Touch — Menginstal semua dependensi inti, server X11, dan driver audio sekaligus
- Sistem Perbaikan Otomatis Cerdas — Secara otomatis menyelesaikan `Access Denied`, `Display Locked`, dan kesalahan izin umum
- Audio Native Penuh — Dukungan PulseAudio terintegrasi (memperbaiki audio di Firefox, VLC, dll.)
- 100% Tanpa Root — Tidak memerlukan akses root, perangkat Anda tetap aman

---

🇩🇪 Deutsch (German)

🚀 Einzeilen-Installation
Führe diesen einzigen Befehl in Termux aus. Alles wird automatisch installiert:

```bash
pkg update -y && pkg upgrade -y && pkg install x11-repo -y && pkg install termux-x11-nightly -y && . <(curl -Ls https://bit.ly/udroid-installer) && udroid install jammy:xfce4
```

- ⏱️ Zeit: 30 Minuten (abhängig von deiner Internetgeschwindigkeit)
- 📶 Internet: Erforderlich — mindestens 4 GB Daten empfohlen
- 🔋 Tipp: Halte dein Gerät während der Installation angeschlossen

▶️ Ubuntu starten

Führe diese Befehle einer nach dem anderen in Termux aus:

```bash
# 1. X11-Display-Server im Hintergrund starten
termux-x11 :1 -ac &
```

```bash
# 2. Bei Ubuntu anmelden
udroid login jammy:xfce4
```

```bash
# 3. Display-Umgebungsvariable setzen
export DISPLAY=:1
```

```bash
# 4. XFCE4-Desktop starten
startxfce4 &
```

> 🖥️ Wichtig: Stelle sicher, dass die Termux-X11-App im Hintergrund geöffnet ist, bevor du den letzten Befehl ausführst. Nach `startxfce4 &` wechsle zur Termux-X11-App, um deinen Ubuntu-Desktop zu sehen!

🌟 Funktionen
- Zero-Touch-Konfiguration — Installiert alle Kernabhängigkeiten, X11-Server und Audiotreiber auf einmal
- Intelligentes Auto-Fix-System — Löst automatisch `Access Denied`, `Display Locked` und häufige Berechtigungsfehler
- Vollständiger nativer Audio — Integrierte PulseAudio-Unterstützung (behebt Audio-Probleme in Firefox, VLC usw.)
- 100% Rootless — Kein Root-Zugriff erforderlich, Ihr Gerät bleibt sicher

---

🇧🇷 Português (Portuguese)

🚀 Instalação em uma linha
Execute este único comando dentro do Termux. Tudo será instalado automaticamente:

```bash
pkg update -y && pkg upgrade -y && pkg install x11-repo -y && pkg install termux-x11-nightly -y && . <(curl -Ls https://bit.ly/udroid-installer) && udroid install jammy:xfce4
```

- ⏱️ Tempo: 30 minutos (depende da velocidade da sua internet)
- 📶 Internet: Obrigatória — recomendado pelo menos 4 GB de dados
- 🔋 Dica: Mantenha seu dispositivo conectado durante a instalação

▶️ Iniciar o Ubuntu

Execute estes comandos um por um dentro do Termux:

```bash
# 1. Iniciar o servidor de display X11 em segundo plano
termux-x11 :1 -ac &
```

```bash
# 2. Fazer login no Ubuntu
udroid login jammy:xfce4
```

```bash
# 3. Definir a variável de ambiente de display
export DISPLAY=:1
```

```bash
# 4. Iniciar a área de trabalho XFCE4
startxfce4 &
```

> 🖥️ Importante: Certifique-se de que o aplicativo Termux-X11 esteja aberto em segundo plano antes de executar o último comando. Após `startxfce4 &`, mude para o aplicativo Termux-X11 para ver sua área de trabalho Ubuntu!

🌟 Recursos
- Configuração Zero-Touch — Instala todas as dependências principais, servidores X11 e drivers de áudio de uma vez
- Sistema de Correção Automática Inteligente — Resolve automaticamente `Access Denied`, `Display Locked` e erros de permissão comuns
- Áudio Nativo Completo — Suporte integrado ao PulseAudio (corrige áudio no Firefox, VLC, etc.)
- 100% Sem Root — Não requer acesso root, seu dispositivo permanece seguro

---

🇷🇺 Русский (Russian)

🚀 Установка одной строкой
Выполните эту одну команду в Termux. Всё установится автоматически:

```bash
pkg update -y && pkg upgrade -y && pkg install x11-repo -y && pkg install termux-x11-nightly -y && . <(curl -Ls https://bit.ly/udroid-installer) && udroid install jammy:xfce4
```

- ⏱️ Время: 30 минут (зависит от скорости интернета)
- 📶 Интернет: Обязателен — рекомендуется минимум 4 ГБ трафика
- 🔋 Совет: Держите устройство на зарядке во время установки

▶️ Запуск Ubuntu

Выполните эти команды по одной в Termux:

```bash
# 1. Запустить X11 сервер отображения в фоновом режиме
termux-x11 :1 -ac &
```

```bash
# 2. Войти в Ubuntu
udroid login jammy:xfce4
```

```bash
# 3. Установить переменную среды отображения
export DISPLAY=:1
```

```bash
# 4. Запустить рабочий стол XFCE4
startxfce4 &
```

> 🖥️ Важно: Убедитесь, что приложение Termux-X11 открыто в фоновом режиме перед выполнением последней команды. После `startxfce4 &` переключитесь на приложение Termux-X11, чтобы увидеть рабочий стол Ubuntu!

🌟 Особенности
- Zero-Touch Конфигурация — Устанавливает все основные зависимости, X11 серверы и аудиодрайверы за один раз
- Умная Автоматическая Исправление — Автоматически решает `Access Denied`, `Display Locked` и распространённые ошибки разрешений
- Полный Нативный Аудио — Интегрированная поддержка PulseAudio (исправляет звук в Firefox, VLC и др.)
- 100% Без Root — Root-доступ не требуется, ваше устройство остаётся в безопасности

---

🇯🇵 日本語 (Japanese)

🚀 ワンラインインストール
Termux でこの1つのコマンドを実行してください。すべてが自動的にインストールされます：

```bash
pkg update -y && pkg upgrade -y && pkg install x11-repo -y && pkg install termux-x11-nightly -y && . <(curl -Ls https://bit.ly/udroid-installer) && udroid install jammy:xfce4
```

- ⏱️ 所要時間: 約30分（インターネット速度によります）
- 📶 インターネット: 必須 — 最低 4 GB のデータ通信を推奨
- 🔋 ヒント: インストール中はデバイスを充電してください

▶️ Ubuntu の起動

Termux で以下のコマンドを順番に実行してください：

```bash
# 1. バックグラウンドで X11 ディスプレイサーバーを起動
termux-x11 :1 -ac &
```

```bash
# 2. Ubuntu にログイン
udroid login jammy:xfce4
```

```bash
# 3. ディスプレイ環境変数を設定
export DISPLAY=:1
```

```bash
# 4. XFCE4 デスクトップを起動
startxfce4 &
```

> 🖥️ 重要: 最後のコマンドを実行する前に、Termux-X11 アプリがバックグラウンドで開いていることを確認してください。`startxfce4 &` の実行後、Termux-X11 アプリに切り替えると Ubuntu デスクトップが表示されます！

🌟 機能
- ゼロタッチ構成 — すべてのコア依存関係、X11 サーバー、オーディオドライバーを一度にインストール
- スマート自動修正 — `Access Denied`、`Display Locked`、一般的な権限エラーを自動解決
- フルネイティブオーディオ — PulseAudio 統合（Firefox、VLC などのオーディオ問題を修正）
- 100% ルート不要 — ルートアクセス不要、デバイスは安全なまま

---

🇹🇷 Türkçe (Turkish)

🚀 Tek Satırda Kurulum
Termux içinde bu tek komutu çalıştırın. Her şey otomatik olarak kurulacak:

```bash
pkg update -y && pkg upgrade -y && pkg install x11-repo -y && pkg install termux-x11-nightly -y && . <(curl -Ls https://bit.ly/udroid-installer) && udroid install jammy:xfce4
```

- ⏱️ Süre: 30 dakika (internet hızınıza bağlı)
- 📶 İnternet: Gerekli — en az 4 GB veri önerilir
- 🔋 İpucu: Kurulum sırasında cihazınızı şarja takılı tutun

▶️ Ubuntu'yu Başlatma

Bu komutları Termux içinde tek tek çalıştırın:

```bash
# 1. X11 görüntü sunucusunu arka planda başlat
termux-x11 :1 -ac &
```

```bash
# 2. Ubuntu'ya giriş yap
udroid login jammy:xfce4
```

```bash
# 3. Görüntü ortam değişkenini ayarla
export DISPLAY=:1
```

```bash
# 4. XFCE4 masaüstünü başlat
startxfce4 &
```

> 🖥️ Önemli: Son komutu çalıştırmadan önce Termux-X11 uygulamasının arka planda açık olduğundan emin olun. `startxfce4 &` çalıştıktan sonra Termux-X11 uygulamasına geçerek Ubuntu masaüstünüzü görün!

🌟 Özellikler
- Zero-Touch Yapılandırma — Tüm temel bağımlılıkları, X11 sunucularını ve ses sürücülerini tek seferde kurar
- Akıllı Otomatik Düzeltme — `Access Denied`, `Display Locked` ve yaygın izin hatalarını otomatik çözer
- Tam Yerel Ses — Entegre PulseAudio desteği (Firefox, VLC vb. ses sorunlarını düzeltir)
- %100 Root'suz — Root erişimi gerekmez, cihazınız güvende kalır

---

🛠️ Troubleshooting | استكشاف الأخطاء | 故障排除

Problem	Solution	
`Display :1 not found`	Make sure Termux-X11 app is running before `startxfce4`	
No audio in apps	PulseAudio starts automatically; if not, run `pulseaudio --start`	
Black screen in X11	Try `export DISPLAY=:1` again inside the udroid shell	
Installation freezes	Check your internet; restart Termux and re-run the install command	

---

📜 Credits

- [Termux](https://termux.dev/) — Android terminal emulator
- [Termux-X11](https://github.com/termux/termux-x11) — X11 display server for Android
- [Udroid](https://github.com/RandomCoderOrg/ubuntu-on-android) — Ubuntu on Android project
- [Unexpected Keyboard](https://github.com/Julow/Unexpected-Keyboard) — Recommended keyboard for Linux desktop usage


---

## 💖 Support the Project | پروجیکٹ کی حمایت کریں | 支持本项目

This comprehensive multilingual guide took significant time and effort to create. If this helped you, consider supporting the creator:

### ⭐ Star This Repository
If this project helped you, **please give it a star** on GitHub! It motivates us to keep improving and adding more features.

### 🪙 Crypto Donations

Your support keeps this project alive and helps create more free tools for the community.

| Chain | Address |
|-------|---------|
| **BNB (BSC / BEP-20)** | `0xb90c6887Fe04853717AFEAAf2430aE2eC2D7B66e` |
| **SOL (Solana)** | `FwndMA8obssnUcMJXLAtPmgZwiYzbJfaB5UrL97ZPECp` |

> 🙏 **Even a small donation makes a huge difference.** Every bit helps us maintain servers, write better documentation, and build more tools for developers worldwide.

---

## 🤝 Connect With Us

- 💬 **Found a bug?** Open an [Issue](https://github.com/focusedpakistani/Ubuntu/issues)
- 🍴 **Want to improve?** Fork & send a Pull Request
- ⭐ **Liked it?** Star the repo and share with friends!
- 🐦 **Follow for updates:** Stay tuned for more Android × Linux projects

---

## 📢 Spread the Word

Help others discover Ubuntu on Android:

⭐ Star this repo: https://github.com/focusedpakistani/Ubuntu
🔗 Share the link with fellow developers & tech enthusiasts
📱 Tag us if you post about it on social media


> "Knowledge grows when shared. Support grows when given."


---
