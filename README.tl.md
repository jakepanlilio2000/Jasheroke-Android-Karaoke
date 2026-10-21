# Jasheroke para sa Android

<img width="1672" height="941" alt="ANDROID" src="https://github.com/user-attachments/assets/cdc60780-fa7c-4080-8d2a-b075295f5750" />

**Bersyon 2.0.0** | StackSync Solutions

[English](README.md) | Tagalog

Gamitin ang Jasheroke bilang karaoke player sa Android o bilang companion para magpareserba ng kanta. Kumanta mula sa iyong lokal na library, magbukas ng reservation room, o sumali sa Windows o Android host gamit ang iyong telepono.

## Pag-download

I-download ang **Jasheroke.apk** mula sa seksiyong **Releases** ng repositoryong ito. Para gawing karaoke host ang Windows PC, i-download ang **Jasheroke.exe** para sa Windows.

| Application | Kasalukuyang bersyon | Gamit |
| --- | --- | --- |
| Jasheroke para sa Android | 2.0.0 | Karaoke player sa Android, reservation host at phone companion |
| Jasheroke para sa Windows | 1.3.0 | Karaoke player sa PC at host ng mga reserbasyon |

## Mga kailangan

- **Android 8.0 o mas bago**.
- Compatible na song library para sa lokal na karaoke playback. May kasama nang SoundFont ang app.
- Iisang lokal na network o Wi-Fi kapag sasali o magbubukas ng reservation room.
- Microphone permission kapag gagamitin ang mga microphone feature.

Sinusuportahan ng APK ang ARM at x86 devices, parehong 32-bit at 64-bit. Hindi kailangan ng lokal na song files o microphone permission para lamang magpareserba gamit ang telepono.

## Mga tampok

- **Library:** maghanap ayon sa pamagat, artist o numero; magpatugtog, magpareserba at mag-save ng paboritong kanta.
- **Phone:** sumali sa host, maghanap sa catalog nito, magpareserba at tingnan ang live queue.
- **Room:** tumanggap ng reserbasyon mula sa telepono, makita ang pangalan ng singer at pamahalaan ang playback at pila.
- **Stage:** landscape na karaoke na may kasabay na lyrics, background videos at mga numero ng nakapilang kanta na nakikita sa itaas.
- **Settings:** dark, light o system na tema, library scanning, pagpili ng SoundFont, backgrounds at permissions.
- Key adjustment na ±6 semitone at tempo na 0.5× hanggang 2×, na naaalala para sa bawat lokal na kanta.
- Mga naka-save na paboritong kanta at pagbabalik ng naputol na reservation queue.

## Pag-install ng app

1. I-download ang `Jasheroke.apk` sa Android device.
2. Buksan ang APK. Kung hilingin ng Android, payagan ang pag-install mula sa browser o file manager na ginamit mo.
3. Tapusin ang pag-install at buksan ang Jasheroke.
4. Buksan ang **Phone** upang sumali sa host, o itakda ang song library sa **Settings** para sa lokal na playback.

## Pagpapareserba sa Windows o Android host

1. Ikonekta ang host at telepono sa iisang lokal na network o Wi-Fi.
2. Magbukas ng room sa host. Sa Windows, gamitin ang **Phones → Start room**. Sa Android, gamitin ang **Room → Open reservation room**.
3. Sa iyong telepono, buksan ang **Phone** at ilagay ang host address, pangalan ng singer at anim na digit na PIN na ipinapakita ng host.
4. Maghanap ng kanta at piliin ang **Reserve**.
5. Buksan ang **Live queue** upang makita ang kasalukuyang kanta at mga naghihintay na reserbasyon.

Halimbawa ng address ang `192.168.1.20:17890`. Sa library ng host naghahanap ang telepono kaya nananatili sa host ang song files. Maaari mong kanselahin ang sarili mong naghihintay na reserbasyon; ang host ang namamahala sa playback, paglaktaw ng kanta at ayos ng pila.

Panatilihing bukas ang host app. Kung Android ang host, panatilihing nasa foreground ang app habang ginagamit ang karaoke. Kapag ni-restart ang room, kailangang sumali muli ang mga bisita.

## Pagkanta sa Android

1. Kopyahin ang compatible na song library sa device at panatilihing nasa iisang folder ang magkaparehang file.
2. Buksan ang **Settings**, gamitin ang **Library access** upang magbigay ng access kung kailangan, at piliin ang song folder.
3. Piliin ang **Save & scan**, pagkatapos ay buksan ang **Library** upang pumili ng kanta.
4. Patugtugin agad o ipareserba ang kanta. Gamitin ang **Room** upang pamahalaan ang pila.

| Uri ng library | Mga kailangang file |
| --- | --- |
| Indexed library | `jashidx` at `jashblob` |
| Paired library | `lyrics.jash` at `mid.jash` |

Hiwalay na inihahanda ang song library at background videos. Gamitin ang kasamang SoundFont o magtakda ng ibang `.sf2` file o folder sa Settings. Maaari ring pumili ng folder para sa background videos.

Upang gumamit ng mikropono, piliin ang **Enable microphone** sa Settings at ibigay ang permission. Makakatulong ang headphones upang mabawasan ang feedback kapag pinapakinggan ang sariling boses.

## Pagbubukas ng reservation room

Ihanda muna ang lokal na library ng Android host, pagkatapos ay piliin ang **Room → Open reservation room**. Ibahagi ang ipinapakitang address at PIN sa mga kakanta. Maaaring sumali ang ibang Android device gamit ang kanilang **Phone** tab.

Ginagamit ng room ang port **17890**. Kailangang maabot ng mga device ang isa't isa sa network. Maaaring humarang sa koneksiyon ang guest Wi-Fi na may device isolation. Maaaring kailangan ding payagan ang Windows host sa Windows Firewall para sa private network.

## Pagbabalik ng session

Kapag naibalik ang na-save na pila, suriin ito at piliing ipagpatuloy. Ang naputol na kanta ay ibabalik sa unahan at magsisimula sa umpisa. Hihintayin ng playback ang iyong pagpili bago magsimula.

## Pag-update ng app

I-install ang bagong release sa ibabaw ng kasalukuyang app upang mapanatili ang settings kapag tinanggap ng Android ang update. Kung may lumang debug installation na iba ang signing certificate, alisin muna iyon bago i-install ang release. Nabubura sa pag-uninstall ang app-private settings at reserbasyon, kaya panatilihin muna ang anumang kailangan mo.

## Paglutas ng problema

| Problema | Dapat suriin |
| --- | --- |
| Hindi makakonekta ang telepono | Suriin ang address, PIN, network at kung bukas ang host. Sumali muli pagkatapos i-restart ang room. |
| Walang laman ang library | Suriin ang library access, napiling folder at magkaparehang library files, pagkatapos ay mag-scan muli. |
| Walang tunog ang MIDI | Suriin ang SoundFont, media volume at audio output. |
| Hindi magamit ang mikropono | Ibigay ang microphone permission sa Settings at suriin ang audio route. |
| Ayaw tanggapin ng Android ang update | Tingnan kung may lumang debug installation na iba ang signing certificate. |

## Pag-uulat ng problema

Gamitin ang seksiyong **Issues** ng repositoryong ito. Isama ang bersyon ng app, modelo ng device, bersyon ng Android, mga hakbang upang maulit ang problema at anumang mensahe ng error. Para sa problema sa reserbasyon, isama ang platform ng host at bersyon ng app nito.

Binuo ng **StackSync Solutions**.
