# maradon-data

Maradon Asistanı uygulamasının indirdiği herkese açık oyun verisi (`game-data.json`).

Knight Online oyuncuları için **resmi olmayan** bir yardımcı araçtır. Knight Online yayıncıları ile bağlantılı değildir.

## Nasıl kullanılır

Uygulama açılışta şu dosyayı indirir:

```
https://raw.githubusercontent.com/heimdilon/maradon-data/main/game-data.json
```

Yeni veri yalnızca doğrulamadan geçerse ve `data_version` mevcut veriden büyükse kabul edilir. Bu yüzden her değişiklikte `data_version` bir artırılmalı ve `updated_at` güncellenmelidir.

## Kurallar

- Saatler sunucu saatidir (`timezone`: `Europe/Istanbul`, UTC+3, yaz saati yok), `HH:MM` biçiminde.
- `days`: 0 = Pazar … 6 = Cumartesi.
- Boss süreleri saniyedir. Sabit süreli bosslarda `min_respawn_sec` = `max_respawn_sec`.
- Uygulama şu an yalnızca `schema_version: 1` ve `Europe/Istanbul` kabul eder.

## Kaynaklar (v2, 2026-11-08)

- Etkinlik saatleri: https://ucuzagb.com/en/guide/etkinlik-saatleri (Türkiye saati). Sınırlı süreli etkinlikler (Arena of Manes, Ultima's Dungeon, Knight Royale) eklenmedi.
- Boss süreleri: https://ucuzagb.com/en/guide/knight-online-boss-saatleri (zamanlı bosslar 32.000 sn = 8 sa 53 dk 20 sn).
- `class_templates`, `weapons` ve `defaults.dura_per_attack` doğrulanmamış örnek değerlerdir.

Bakım veya yama sonrası saatler kayabilir; oyun içi duyurular önceliklidir.
