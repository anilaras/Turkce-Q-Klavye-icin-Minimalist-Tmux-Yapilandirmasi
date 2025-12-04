# Linux & Türkçe Q Klavye için Minimalist Tmux Yapılandırması
Bu depo, Linux ortamında Türkçe Q klavye kullanan geliştiriciler için ergonomik, hızlı ve "font bağımsız" (kurulum gerektirmeyen) bir `tmux` yapılandırması sunar.

Varsayılan tmux kısayolları (özellikle `[` ve `]`) Türkçe klavye düzeninde `AltGr` kombinasyonları gerektirdiğinden oldukça verimsizdir. Bu yapılandırma, **Vim** tuş düzenini temel alır ve özel font yüklemeye gerek kalmadan sade bir arayüz sunar.
## Özellikler

-   **Evrensel Görünüm:** Powerline veya Nerd Font gerektirmez. Her terminalde sorunsuz çalışır.
    
-   **Ergonomik Prefix:** `Ctrl+b` yerine `Ctrl+a` (Serçe parmak dostu).
    
-   **Akıllı Bölme (Splitting):** `AltGr` gerektiren karakterler yerine anımsatıcı tuşlar (`v`ertical, `s`plit).
    
-   **Vim Tarzı Gezinti:** Paneller arasında `h`, `j`, `k`, `l` ile gezinti.
    
-   **Kolay Kopyalama:** `Esc` ile moda gir, `v` ile seç, `y` ile sistem panosuna (clipboard) kopyala.
    
-   **Oturum Sürekliliği:** Bilgisayarı yeniden başlatsanız bile oturumlarınız geri yüklenir.
    

## Kurulum

### 1. Gereksinimler

Sistem panosuna kopyalama yapabilmek için `xclip` aracının yüklü olması önerilir:

Bash

```
# Ubuntu / Debian
sudo apt install xclip

# Arch Linux
sudo pacman -S xclip

```

### 2. Tmux Plugin Manager (TPM) Kurulumu

Eklentilerin çalışması için TPM'i kurmalısınız:

Bash

```
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm

```

### 3. Yapılandırmayı Uygulama

Bu repodaki `.tmux.conf` dosyasını ana dizininize (`~/.tmux.conf`) kopyalayın. Ardından terminalde şu komutu çalıştırarak eklentileri yükleyin:

1.  Tmux'ı açın: `tmux`
    
2.  Eklentileri yüklemek için: `Ctrl` + `a` ardından `I` (Büyük I harfi) tuşuna basın.
    

## ⌨️ Kısayol Referansı
|Eylem| Kısayol | Not |
|--|--|--|
|**Prefix (Öncül Tuş)**  | `Ctrl` + `a` | Tüm komutlardan önce basılır. |
|**Config Yenile**  | `prefix` + `r` |Yapılandırma dosyasını reload eder.|
|**Dikey Böl (Vertical)** | `prefix` + `v` | Yan yana böler. |
|**Yatay Böl (Split)**| `prefix` + `s`| Alt alta böler.|
|**Panel Gezintisi**| `prefix` + `h/j/k/l`| Vim yön tuşları ile gezinti. |
|**Hızlı Panel Gezintisi**  | `Alt` + `Yön Tuşları`| Prefix'e basmadan hızlı geçiş.|
|**Kopyalama Modu**| `prefix` + `Esc` | Kopyalama moduna girer. |
|**Seçim yapma**| `v` | Kopyalama modunda seçimi başlatır.|
|**Kopyala (yank)**| `y` | Seçimi sistem panosuna kopyalar.|
