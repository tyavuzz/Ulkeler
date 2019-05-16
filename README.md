microsoft sql server dünyadaki ülkeler, ülkelerin illeri, illerin ilçeleri.

ülke ilk ilçe çeklinde listeleyebilimek için 

SELECT dbo.ULKELER.NAME 'Ülke Adi',
       dbo.SEHIRLER.NAME AS 'sehir Adi',
       dbo.ILCELER.NAME AS 'İlçe Adi'
FROM dbo.ULKELER
    INNER JOIN dbo.SEHIRLER
        ON dbo.ULKELER.ID = dbo.SEHIRLER.ULKE_ID
    INNER JOIN dbo.ILCELER
        ON dbo.SEHIRLER.ID = dbo.ILCELER.SEHIR_ID;
