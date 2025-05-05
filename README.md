<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8">
  <title>Osmanlıca - Türkçe Sözlük (Gelişmiş)</title>
  <style>
    body { font-family: Arial, sans-serif; padding: 30px; background: #f9f9f9; }
    select, #meaning { font-size: 18px; margin-top: 20px; padding: 8px; width: 350px; }
    h1 { color: #2c3e50; }
    #meaning { margin-top: 30px; font-weight: bold; }
  </style>
</head>
<body>
  <h1>Zor Osmanlıca Kelimeler - Sözlük</h1>

  <label for="wordSelect">Bir Osmanlıca kelime seçin:</label><br>
  <select id="wordSelect">
    <option value="">-- Kelime Seçin --</option>
    <option value="müteşekkir">Müteşekkir</option>
    <option value="mübhem">Mübhem</option>
    <option value="mütereddit">Mütereddit</option>
    <option value="serlevha">Serlevha</option>
    <option value="suikast">Suikast</option>
    <option value="müzahrefat">Müzahrefat</option>
    <option value="meşveret">Meşveret</option>
    <option value="mütalaa">Mütalaa</option>
    <option value="irşad">İrşad</option>
    <option value="müteallik">Müteallik</option>
    <option value="mücahede">Mücahede</option>
    <option value="tebellür">Tebellür</option>
    <option value="tahakküm">Tahakküm</option>
    <option value="tesir">Tesir</option>
    <option value="mütareke">Mütareke</option>
    <option value="tagallüb">Tagallüb</option>
    <option value="müzaheret">Müzaheret</option>
    <option value="mübaşeret">Mübaşeret</option>
    <option value="tebellüat">Tebellüat</option>
    <option value="mükellef">Mükellef</option>
    <option value="tecavüz">Tecavüz</option>
    <option value="müsamaha">Müsamaha</option>
    <option value="temeddün">Temeddün</option>
    <option value="mukadderat">Mukadderat</option>
    <option value="teşebbüs">Teşebbüs</option>
    <option value="taalluk">Taalluk</option>
    <option value="temerrüd">Temerrüd</option>
    <option value="tevazu">Tevazu</option>
    <option value="mukavemet">Mukavemet</option>
    <option value="müsademe">Müsademe</option>
    <option value="tahliye">Tahliye</option>
    <option value="müfrit">Müfrit</option>
    <option value="muvazene">Muvazene</option>
    <option value="taksirat">Taksirat</option>
    <option value="tevdi">Tevdi</option>
    <option value="müstacel">Müstacel</option>
    <option value="tecviz">Tecviz</option>
    <option value="suret-i katiye">Suret-i katiye</option>
    <option value="istirdat">İstirdat</option>
    <option value="intibah">İntibah</option>
    <option value="teyakkuz">Teyakkuz</option>
    <option value="mücerret">Mücerret</option>
    <option value="menfi">Menfi</option>
    <option value="müzmin">Müzmin</option>
    <option value="muktesit">Muktesit</option>
    <option value="tahakkuk">Tahakkuk</option>
    <option value="müteyakkız">Müteyakkız</option>
    <option value="müheyyiç">Müheyyiç</option>
    <option value="tefekkür">Tefekkür</option>
    <option value="teşri">Teşri</option>
  </select>

  <div id="meaning"></div>

  <script>
    const dictionary = {
      "müteşekkir": "Minnettar, teşekkür eden",
      "mübhem": "Belirsiz, açık olmayan",
      "mütereddit": "Kararsız, tereddüt eden",
      "serlevha": "Başlık",
      "suikast": "Kötü niyetle öldürme girişimi",
      "müzahrefat": "Pislik, atık",
      "meşveret": "Danışma, istişare",
      "mütalaa": "İnceleme, okuma değerlendirmesi",
      "irşad": "Doğru yolu gösterme",
      "müteallik": "İlgili, ilişik",
      "mücahede": "Çaba gösterme, mücadele etme",
      "tebellür": "Açığa çıkma, belirginleşme",
      "tahakküm": "Baskı kurma, egemenlik",
      "tesir": "Etki",
      "mütareke": "Ateşkes",
      "tagallüb": "Üstünlük kurma, galip gelme",
      "müzaheret": "Yardım etme",
      "mübaşeret": "Cinsel ilişki",
      "tebellüat": "Tebliğler, bildiriler",
      "mükellef": "Yükümlü, sorumlu",
      "tecavüz": "Saldırma, ihlal",
      "müsamaha": "Hoşgörü",
      "temeddün": "Medenileşme",
      "mukadderat": "Kader, alın yazısı",
      "teşebbüs": "Girişim, deneme",
      "taalluk": "İlişki kurma, ilgilenme",
      "temerrüd": "İsyan etme, karşı gelme",
      "tevazu": "Alçakgönüllülük",
      "mukavemet": "Direnme, dayanma",
      "müsademe": "Çarpışma",
      "tahliye": "Boşaltma, serbest bırakma",
      "müfrit": "Aşırıya giden, ifrata kaçan",
      "muvazene": "Denge",
      "taksirat": "Eksiklikler, kusurlar",
      "tevdi": "Teslim etme, verme",
      "müstacel": "Acele olan, hemen gereken",
      "tecviz": "Uygun bulma, izin verme",
      "suret-i katiye": "Kesin biçimde",
      "istirdat": "Geri alma",
      "intibah": "Uyanış, farkına varma",
      "teyakkuz": "Uyanıklık, tetikte olma",
      "mücerret": "Bekâr, evli olmayan / soyut",
      "menfi": "Olumsuz, negatif",
      "müzmin": "Sürekli, kronik",
      "muktesit": "İtidalli, ölçülü",
      "tahakkuk": "Gerçekleşme",
      "müteyakkız": "Dikkatli, uyanık",
      "müheyyiç": "Tahrik edici, kışkırtıcı",
      "tefekkür": "Düşünme, derin düşünce",
      "teşri": "Kanun koyma"
    };

    document.getElementById('wordSelect').addEventListener('change', function() {
      const selected = this.value;
      const meaning = dictionary[selected] || "";
      document.getElementById('meaning').innerHTML = meaning ? 
        `<p><strong>Yeni Türkçesi:</strong> ${meaning}</p>` : "";
    });
  </script>
</body>
</html>
