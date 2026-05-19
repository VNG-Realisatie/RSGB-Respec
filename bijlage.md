# Bijlage 1: Relatie tot GFO Basisgegevens

In dit referentiemodel hebben we het GFO BasisGegevens niet compleet overgenomen. Zie voor de motivering hiervan bijlage 1 van het RSGB versie 1.0. Hieronder geven we per gegevensgroep (in het GFO BG) aan welke gegevens wel en welke niet zijn overgenomen.


Onderstaande tabel geeft de overeenkomsten en verschillen weer van het GFO-BG ten opzichte van het RSGB. De object- en gegevenstypen die deel uit maken van het RSGB, maar niet in het GFO-BG waren opgenomen, staan niet vermeld.
De eerste kolom vermeldt de onderscheiden gegevensgroepen (vet gedrukt) en gegevens in het GFO-BG. In de tweede kolom staat het objecttype uit het RSGB, dat overeenkomt met de GFO-BG-gegevensgroep, dan wel het objecttype waarbij het gegeven is opgenomen. In de derde kolom staat een toelichting, als die nodig is.

| Gegevensgroep resp. gegeven in GFO-BG | Objecttype | Opmerking |
|---|---|---|
| **Academische Titel** | ACADEMISCHE TITEL | |
| *Academische titel van een natuurlijk persoon | | |
| Academische titelcode | | |
| Omschrijving academische titel | | |
| Positie academische titel t.o.v. naam | | |
| **Adellijke Titel/Predikaat** | NATUURLIJK PERSOON | De attribuutsoorten van de GBA zijn aangehouden, waardoor de GFO-BG-gegevens niet één op één overeenkomen. |
| *Adellijke titel/predikaat van een natuurlijk persoon | NATUURLIJK PERSOON | |
| Adellijke titel of predikaat (code) | NATUURLIJK PERSOON | |
| Omschrijving adellijke titel | NATUURLIJK PERSOON | |
| Soort adellijke titel/predikaat | NATUURLIJK PERSOON | |
| **Adres** | ADRESSEERBAAR OBJECT AANDUIDING | Alleen gemodelleerd als Locatie-adres (in de terminologie van het GFO-BG) dus niet als Postadres. Betreft alleen officiële adressen. |
| *Correspondentieadres | ADRESSEERBAAR OBJECT AANDUIDING | |
| *Inschrijvingsadres | VERBLIJFSOBJECT, STANDPLAATS en LIGPLAATS TERREIN | Gemodelleerd als 'verblijft in of op'. |
| Postcode | ADRESSEERBAAR OBJECT AANDUIDING | |
| Woonplaatsnaam | WOONPLAATS | |
| **Adresfiliatie** | - | Niet opgenomen aangezien de filiatie van GEBOUWD OBJECT en BENOEMD TERREIN bepalend is. |
| *Adresfiliatie is ontstaan uit locatieadres | - | |
| *Adresfiliatie is overgegaan in locatieadres | - | |
| Filiatiecode locatieadres | - | |
| **Bestemmingsgebied** | - | Het Bestemmingsgebied is niet opgenomen met het oog op de ontwikkelingen rondom Imro en DURP waarbij sprake zou kunnen zijn van een geografische registratie van bestemmingen. |
| *Bestemming van een kadastraal object | - | |
| *Bestemming van een overig bouwwerk | - | |
| *Bestemming van een verblijfsobject | - | |
| Bestemmingsplanherziening | - | |
| Naam bestemmingsplan | - | |
| Omschrijving bestemmingsgebied | - | |
| Omschrijving planologische bestemming | GEBOUWD OBJECT | |
| **Bouwwerk** | - | Bebouwing is in de BGR anders gemodelleerd, het niveau Bouwwerk komt niet meer voor. |
| *Gebouw is onderdeel van bouwwerk | - | |
| *Overig bouwwerk is onderdeel van bouwwerk | - | |
| Bouwwerknummer | - | |
| **Buurt** | BUURT | |
| *Buurt bij een locatieadres | BUURT | De relatie is verlegd naar GEBOUWD OBJECT en BENOEMD TERREIN |
| *Buurt in een wijk | BUURT | |
| Buurtcode | BUURT | |
| Buurtnaam | BUURT | |
| Einddatum buurt | BUURT | |
| Ingangsdatum buurt | BUURT | |
| **Filiatie kadastraal object** | KADASTRALE ONROERENDE ZAAK HISTORIE RELATIE | |
| *Filiatie kadastraal object is ontstaan uit kadastraal object | | |
| *Filiatie kadastraal object is overgegaan in kadastraal object | | |
| Filiatiecode kadastraal object | | |
| **Filiatie verblijfsobject** | BENOEMD OBJECT | Gemodelleerd als n:m-relatie van het object zelf. |
| *Filiatie verblijfsobject is ontstaan uit verblijfsobject | | |
| *Filiatie verblijfsobject is overgegaan in verblijfsobject | | |
| Filiatiecode verblijfsobject | | |
| **Gebouw** | - | Bebouwing is in de BGR anders gemodelleerd, het niveau Gebouw komt niet meer voor. |
| *Gebouw is onderdeel van bouwwerk | - | |
| *Pand is onderdeel van gebouw | - | |
| Gebouwnummer | - | |
| **Gemeente** | GEMEENTE | |
| *Gemeente van inschrijving | INGESCHREVEN PERSOON | |
| *Gemeente waarin locatieadres ligt | - | Gemodelleerd naar GEBOUWD OBJECT, LIGPLAATS en STANDPLAATS via WOONPLAATS, OPENBARE RUIMTE en ADRESSEERBAAR OBJECT AANDUIDING. |
| *Wijk in een gemeente | GEMEENTE | |
| Einddatum gemeente | GEMEENTE | |
| Gemeente waarin overgegaan | GEMEENTE | |
| Gemeentecode | GEMEENTE | |
| Gemeentenaam | GEMEENTE | |
| Ingangsdatum gemeente | GEMEENTE | |
| **Huishouden** | HUISHOUDEN | |
| *Huishouden heeft huishoudenrelaties | HUISHOUDEN | |
| *Huishouden is gehuisvest in WOZ-object | HUISHOUDEN | Relatie is niet gelegd naar het WOZ-object maar naar het VERBLIJFSOBJECT, LIGPLAATS en STANDPLAATS. |
| Grootte huishouden | HUISHOUDEN | |
| Huishoudennummer | HUISHOUDEN | |
| Soort huishouden | HUISHOUDEN | |
| **Huishoudenrelatie** | HUISHOUDENRELATIE | |
| *Huishouden heeft huishoudenrelaties | HUISHOUDENRELATIE | |
| *Huishoudenrelatie is een natuurlijk persoon | HUISHOUDENRELATIE | Relatie is gelegd naar INGESCHREVEN PERSOON |
| Einddatum huishoudenrelatie | HUISHOUDENRELATIE | |
| Huishoudenrelatiecode | HUISHOUDENRELATIE | metagegeven |
| Ingangsdatum huishoudenrelatie | HUISHOUDENRELATIE | metagegeven |
| **Huwelijk/Geregistreerd partnerschap** | HUWELIJK / GEREGISTREERD PARTNERSCHAP | Uitgegaan is van de GBA, alle desbetreffende gegevens zijn overgenomen. |
| *Huwelijk/partnerschap bestaat uit | | |
| *Land huwelijkssluiting/aangaan geregistreerd partnerschap | | |
| *Land ontbinding huwelijk/geregistreerd partnerschap | | |
| Datum huwelijkssluiting/aangaan geregistreerd partnerschap | | |
| Datum inschrijving vonnis ontbinding huwelijk/geregistreerd | | |
| Datum ontbinding huwelijk/geregistreerd partnerschap | | |
| Plaats huwelijkssluiting/aangaan geregistreerd partnerschap | | |
| Plaats ontbinding huwelijk/geregistreerd partnerschap | | |
| Reden ontbinding huwelijk/geregistreerd partnerschap | | |
| Soort verbintenis | | |
| **Kadastraal object** | KADASTRALE ONROERENDE ZAAK | |
| *Bestemming van een kadastraal object | - | Gemodelleerd vanuit GEBOUWD OBJECT. |
| *Filiatie kadastraal object is ontstaan uit kadastraal object | KADASTRALE ONROERENDE ZAAK | |
| *Filiatie kadastraal object is overgegaan in kadastraal object | KADASTRALE ONROERENDE ZAAK | |
| *Kadastraal object bij een overig bouwwerk | - | Overig Bouwwerk is vervallen, zie toelichting aldaar. |
| *Kadastraal object bij een verblijfsobject | KADASTRALE ONROERENDE ZAAK | Relatie is gemodelleerd naar GEBOUWD OBJECT, LIGPLAATS en STANDPLAATS. |
| *Kadastraal object bij een WOZ-object | KADASTRALE ONROERENDE ZAAK | |
| *Locatieadres van een kadastraal object | KADASTRALE ONROERENDE ZAAK | Relatie naar adres loopt via GEBOUWD OBJECT, LIGPLAATS en STANDPLAATS. |
| *Publiekrechtelijke beperking rust op kadastraal object | - | Publiekrechtelijke Beperking is niet opgenomen, zie toelichting aldaar. |
| *Voornaamste zakelijk gerechtigde | KADASTRALE ONROERENDE ZAAK | |
| *Zakelijk recht rust op kadastraal object | KADASTRALE ONROERENDE ZAAK | |
| Aanduiding indicatie mogelijk | - | Zie opmerking bij Publiekrechtelijke Beperking. |
| Centroïd x-coördinaat kadastraal object | KADASTRAAL PERCEEL | |
| Centroïd y-coördinaat kadastraal object | | |
| Centroïd z-coördinaat kadastraal object | | |
| Einddatum kadastraal object | KADASTRAAL OBJECT | |
| Indicatie oppervlakte geschat | KADASTRAAL PERCEEL | Gegeventype 'Aanduiding soort grootte'. |
| Indicatie vervallen | KADASTRAAL OBJECT | Gegeventype 'Vervallen o.b.v. stuk'. |
| Ingangsdatum kadastraal object | KADASTRAAL OBJECT | |
| Kadastraal object index letter | KADASTRAAL PERCEEL en APPARTEMENTSRECHT | Via Kadastrale onroerende zaak typering |
| Kadastraal object index nummer | KADASTRAAL PERCEEL en APPARTEMENTSRECHT | |
| Kadastraal perceelnummer | KADASTRAAL OBJECT | |
| Kadastrale gemeentecode | KADASTRAAL OBJECT | |
| Kadastrale sectie | KADASTRAAL OBJECT | |
| Omschrijving deelperceel | KADASTRAAL PERCEEL | |
| Oppervlakte kadastraal object | KADASTRAAL PERCEEL | |
| **Land** | LAND | |
| *Geboorteland | NATUURLIJK PERSOON | |
| *Land huwelijkssluiting/aangaan geregistreerd partnerschap | PARTNERRELATIE | |
| *Land ontbinding huwelijk/geregistreerd partnerschap | PARTNERRELATIE | |
| *Land overlijden | INGESCHREVEN PERSOON | |
| *Land van emigratie | INGESCHREVEN PERSOON | |
| *Land van immigratie | INGESCHREVEN PERSOON | |
| *Land waarin postadres ligt | SUBJECT | |
| Einddatum land | LAND | Zie opmerking hierboven. |
| Ingangsdatum land | LAND | |
| Landcode | LAND | |
| Landnaam | LAND | |
| **Locatieadres** | ADRESSEERBAAR OBJECT AANDUIDING | |
| *Adresfiliatie is ontstaan uit locatieadres | - | Niet opgenomen aangezien de filiatie van BENOEMD OBJECT bepalend is. |
| *Adresfiliatie is overgegaan in locatieadres | - | |
| *Buurt bij een locatieadres | BENOEMD OBJECT | De relatie naar BUURT is verlegd naar genoemd objecttype. |
| *Gemeente waarin locatieadres ligt | WOONPLAATS | Relatie verloopt via OPENBARE RUIMTE en WOONPLAATS. |
| *Hoofdadres van een WOZ-object | ADRESSEERBAAR OBJECT AANDUIDING | Ook via BENOEMD OBJECT. |
| *Locatieadres van een kadastraal object | GEBOUWD OBJECT, LIGPLAATS en STANDPLAATS | De relatie naar KADASTRAAL OBJECT is verlegd naar genoemde objecttypen. |
| *Locatieadres van een overig bouwwerk | OVERIG GEBOUWD OBJECT | Overig Bouwwerk komt niet meer voor. In de relatie is voorzien d.m.v. het OVERIG GEBOUWD OBJECT |
| *Locatieadres van een verblijfsobject | ADRESSEERBAAR OBJECT AANDUIDING | |
| *Nevenadres van een WOZ-object | - | WOZ-object kent slechts één WOZ-adres. |
| *Verblijfs/vestigingsadres | VERBLIJFSOBJECT, LIGPLAATS EN STANDPLAATS | De relatie is verlegd naar genoemde objecttypen. |
| *Wijk bij een locatieadres | BUURT | De relatie verloopt via BENOEMD OBJECT en BUURT. |
| Aanduiding bij huisnummer | - | Maakt geen deel meer uit van een officieel adres. |
| Centroïd x-coördinaat locatieadres | GEBOUWD OBJECT | |
| Centroïd y-coördinaat locatieadres | GEBOUWD OBJECT | |
| Centroïd z-coördinaat locatieadres | - | Maakt vooralsnog geen deel uit van de BAG. |
| Einddatum locatieadres | ADRESSEERBAAR OBJECT AANDUIDING | |
| Huisletter | ADRESSEERBAAR OBJECT AANDUIDING | |
| Huisnummer | ADRESSEERBAAR OBJECT AANDUIDING | |
| Huisnummertoevoeging | ADRESSEERBAAR OBJECT AANDUIDING | |
| Ingangsdatum locatieadres | ADRESSEERBAAR OBJECT AANDUIDING | |
| Locatieadresnummer | ADRESSEERBAAR OBJECT AANDUIDING | Identificatiecode adresseerbaar object aanduiding |
| Locatieomschrijving | OVERIG GEBOUWD OBJECT | De Locatieomschrijving maakt geen deel uit van een officieel adres. Wel kan het bij het OVERIG GEBOUWD OBJECT worden gebruikt om de ligging ervan t.o.v. een officiële ADRESSEERBAAR OBJECT AANDUIDING of een OPENBARE RUIMTE aan te geven. |
| Straatcode | (GEMEENTELIJKE) OPENBARE RUIMTE | Identificatiecode (gemeentelijke) openbare ruimte |
| Straatnaam | GEMEENTELIJKE OPENBARE RUIMTE | |
| **Nationaliteit** | NATIONALITEIT | |
| *Code van een nationaliteit | | |
| Einddatum nationaliteit | | |
| Ingangsdatum nationaliteit | | |
| Nationaliteit (code) | | |
| Omschrijving nationaliteit | | |
| **Natuurlijk persoon** | NATUURLIJK PERSOON en specialisaties daarvan | |
| *Academische titel van een natuurlijk persoon | NATUURLIJK PERSOON | |
| *Adellijke titel/predikaat van een natuurlijk persoon | NATUURLIJK PERSOON | |
| *Geboorteland | INGESCHREVEN PERSOON | |
| *Gemeente van inschrijving | INGESCHREVEN PERSOON | |
| *Huishoudenrelatie is een natuurlijk persoon | INGESCHREVEN PERSOON | |
| *Huwelijk/partnerschap bestaat uit | INGESCHREVEN PERSOON | |
| *Identiteitsbewijs van een natuurlijk persoon | INGESCHREVEN PERSOON | |
| *Inschrijvingsadres | INGESCHREVEN PERSOON | |
| *Kind heeft moeder | INGESCHREVEN PERSOON | |
| *Kind heeft vader | INGESCHREVEN PERSOON | |
| *Land overlijden | INGESCHREVEN PERSOON | |
| *Land van emigratie | INGESCHREVEN PERSOON | |
| *Land van immigratie | INGESCHREVEN PERSOON | |
| *Nationaliteit van een natuurlijk persoon | INGESCHREVEN PERSOON | |
| *Ouder heeft kind | INGESCHREVEN PERSOON | |
| *Verblijfstitel van een natuurlijk persoon | INGESCHREVEN PERSOON | |
| A-nummer | INGESCHREVEN PERSOON | |
| Aanduiding bijzonder Nederlanderschap | INGESCHREVEN PERSOON | |
| Aanduiding naamgebruik | NATUURLIJK PERSOON | |
| Burgerlijke staat | HUWELIJK / GEREGISTREERD PARTNERSCHAP | |
| Datum inschrijving in gemeente | INGESCHREVEN PERSOON | |
| Datum opschorting bijhouding | INGESCHREVEN PERSOON | metagegeven |
| Datum overlijden | NATUURLIJK PERSOON | |
| Datum verkrijging verblijfstitel | INGEZETENE | |
| Datum verlies verblijfstitel | INGEZETENE | |
| Datum vertrek uit Nederland | INGESCHREVEN PERSOON | |
| Datum vestiging in Nederland | INGESCHREVEN PERSOON | |
| Geboortedatum | NATUURLIJK PERSOON | |
| Geboorteplaats | INGESCHREVEN PERSOON | |
| Geslachtsaanduiding | NATUURLIJK PERSOON | |
| Geslachtsnaam | NATUURLIJK PERSOON | |
| Indicatie curateleregister | INGEZETENE | |
| Indicatie geheim | INGESCHREVEN PERSOON | |
| Indicatie gezag minderjarige | INGEZETENE | |
| Omschrijving reden opschorting bijhouding | INGESCHREVEN PERSOON | |
| Plaats overlijden | INGESCHREVEN PERSOON | |
| Voorletters | NATUURLIJK PERSOON | |
| Voornamen | NATUURLIJK PERSOON | |
| Voorvoegsel geslachtsnaam | NATUURLIJK PERSOON | |
| **Nevenvestiging** | VESTIGING | |
| *Nevenvestiging | VESTIGING | Attribuutsoort 'Typering hoofd/nevenvestiging'. |
| **Niet-natuurlijk persoon** | NIET-NATUURLIJK PERSOON, MAATSCHAPPELIJKE ACTIVITEIT en VESTIGING | |
| *Hoofdactiviteit | MAATSCHAPPELIJKE ACTIVITEIT en VESTIGING | Gegeventype 'NACE-code'. |
| *Nevenactiviteit | MAATSCHAPPELIJKE ACTIVITEIT en VESTIGING | Gegeventype 'NACE-code'. |
| *Nevenvestiging | VESTIGING | Attribuutsoort 'Typering hoofd/nevenvestiging'. |
| *Rechtsvorm van een niet-natuurlijk persoon | NIET-NATUURLIJK PERSOON | |
| Aantal werkzame mannen fulltime | - | |
| Aantal werkzame mannen parttime | - | |
| Aantal werkzame vrouwen fulltime | - | |
| Aantal werkzame vrouwen parttime | - | |
| Datum einde niet-natuurlijk persoon | INGESCHREVEN NIET-NATUURLIJK PERSOON | |
| Datum ontbinding niet-natuurlijk persoon | INGESCHREVEN NIET-NATUURLIJK PERSOON | |
| Datum oprichting niet-natuurlijk persoon | INGESCHREVEN NIET-NATUURLIJK PERSOON | |
| Handelsnaam | MAATSCHAPPELIJKE ACTIVITEIT en VESTIGING | |
| Handelsregisternummer | MAATSCHAPPELIJKE ACTIVITEIT | KvK-nummer |
| Indicatie faillissement | - | |
| Indicatie hoofdvestiging | VESTIGING | Attribuutsoort 'Typering hoofd/nevenvestiging'. |
| Indicatie surséance van betaling | - | |
| Soort niet-natuurlijk persoon | - | |
| Statutaire naam / Vennootschapsnaam | NIET-NATUURLIJK PERSOON | |
| Zaaknaam | MAATSCHAPPELIJKE ACTIVITEIT en VESTIGING | Het NHR kent de handelsnaam. |
| **Niet-woonobject** | GEBOUWD OBJECT | |
| Aantal parkeerplaatsen | - | |
| Frontbreedte | - | |
| **Ouder-Kind** | OUDER-KIND-RELATIE | |
| *Kind heeft moeder | OUDER-KIND-RELATIE | |
| *Kind heeft vader | OUDER-KIND-RELATIE | |
| *Ouder heeft kind | OUDER-KIND-RELATIE | |
| Einddatum familierechtelijke betrekking | OUDER-KIND-RELATIE | |
| Ingangsdatum familierechtelijke betrekking | OUDER-KIND-RELATIE | |
| **Overig bouwwerk** | OVERIG GEBOUWD OBJECT | |
| *Bestemming van een overig bouwwerk | GEBOUWD OBJECT | |
| *Kadastraal object bij een overig bouwwerk | GEBOUWD OBJECT | |
| *Locatieadres van een overig bouwwerk | OVERIG GEBOUWD OBJECT | |
| *Overig bouwwerk behoort tot WOZ-object | OVERIG GEBOUWD OBJECT | |
| *Overig bouwwerk is onderdeel van bouwwerk | - | Zie opmerking bij Bouwwerk. |
| Omschrijving overig bouwwerk | - | |
| Overig-bouwwerknummer | GEBOUWD OBJECT | |
| Type overig bouwwerk | OVERIG GEBOUWD OBJECT | |
| **Pand** | PAND | De definitie en daarmee de afbakening van een PAND is anders dan die in het GFO-BG. |
| *Pand is onderdeel van gebouw | - | Zie opmerking bij Gebouw. |
| *Verblijfsobject is onderdeel van pand | PAND | |
| Hoogste bouwlaag pand | PAND | |
| Laagste bouwlaag pand | PAND | |
| Pandnummer | PAND | |
| **Persoonlijk identiteitsbewijs** | REISDOCUMENT | |
| *Identiteitsbewijs van een natuurlijk persoon | | |
| *Soort identiteitsbewijs | | |
| Nummer identiteitsbewijs | | |
| **Persoonlijke nationaliteit** | INGESCHREVEN PERSOON | |
| *Code van een nationaliteit | INGESCHREVEN PERSOON | |
| *Nationaliteit van een natuurlijk persoon | INGESCHREVEN PERSOON | |
| Datum verkrijging nationaliteit | INGESCHREVEN PERSOON | |
| Datum verlies nationaliteit | INGESCHREVEN PERSOON | |
| **Postadres** | - | Is niet meer als separaat objecttype gemodelleerd. |
| *Land waarin postadres ligt | SUBJECT | |
| Adres buitenland (1) | SUBJECT | |
| Adres buitenland (2) | | |
| Adres buitenland (3) | | |
| Adres buitenland (4) | - | |
| Antwoordnummer | SUBJECT | |
| Postbusnummer | SUBJECT | |
| **Publiekrechtelijke beperking** | - | |
| *Code van een publiekrechtelijke beperking | - | |
| *Publiekrechtelijke beperking rust op kadastraal object | - | |
| Einddatum publiekrechtelijke beperking | - | |
| Ingangsdatum publiekrechtelijke beperking | - | |
| Vindplaats document | - | |
| **SBI-codering** | - | Overeenkomstig het NHR niet separaat gemodelleerd. |
| *Hoofdactiviteit | - | |
| *Nevenactiviteit | - | |
| SBI-code | VESTIGING | Gegeventype 'NACE-code'. |
| SBI-omschrijving | VESTIGING | Gegeventype 'NACE-code'. |
| **Soort identiteitsbewijs** | REISDOCUMENT SOORT | |
| *Soort identiteitsbewijs | | |
| Identiteitsbewijs (code) | | |
| Omschrijving identiteitsbewijs | | |
| **Soort publiekrechtelijke beperking** | - | |
| *Code van een publiekrechtelijke beperking | - | |
| Publiekrechtelijke beperking code | - | |
| Publiekrechtelijke beperking omschrijving | - | |
| **Soort rechtsvorm** | - | Overeenkomstig het NHR niet separaat gemodelleerd. |
| *Rechtsvorm van een niet-natuurlijk persoon | - | |
| Rechtsvormcode | NIET-NATUURLIJK PERSOON | |
| Rechtsvormomschrijving | NIET-NATUURLIJK PERSOON | |
| **Soort zakelijk recht** | AARD VERKREGEN RECHT | Overeenkomstig de BRK niet separaat gemodelleerd. |
| *Code van een zakelijk recht | AARD VERKREGEN RECHT | |
| Aanduiding erfdienstbaarheid | - | |
| Zakelijk recht omschrijving | AARD VERKREGEN RECHT | |
| Zakelijk-rechtcode | AARD VERKREGEN RECHT | |
| **Subject** | SUBJECT | |
| *Correspondentieadres | SUBJECT | |
| *Eigenaar | - | Gemodelleerd via ZAKELIJK RECHT. |
| *Gebruiker | - | Gemodelleerd als relatie met VERBLIJFSOBJECT, STANDPLAATS EN LIGPLAATS voor INGESCHREVEN PERSOON en via VESTIGING voor NIET-NATUURLIJK PERSOON. |
| *Subject heeft zakelijk recht | SUBJECT | |
| *Verblijfs/vestigingsadres | INGESCHREVEN PERSOON | |
| *Voornaamste zakelijk gerechtigde | RECHTSPERSOON | |
| Aanvulling Sofi-nummer | NIET-NATUURLIJK PERSOON | NNP-ID |
| Bank/girorekeningnummer | SUBJECT | |
| E-mail adres | SUBJECT | |
| Faxnummer | SUBJECT | |
| Sofi-nummer | - | Wel: BurgerServiceNummer (bij INGESCHREVEN PERSOON) en NNP-ID (bij NIET-NATUURLIJK PERSOON). |
| Subjectnummer AKR | - | |
| Telefoonnummer | SUBJECT | |
| **Verblijfsobject** | VERBLIJFSOBJECT | In sommige gevallen kan dit een OVERIG GEBOUWD OBJECT of BENOEMD TERREIN zijn aangezien de definitie van verblijfsobject verschilt tussen de BGR en het GFO-BG. |
| *Bestemming van een verblijfsobject | GEBOUWD OBJECT | |
| *Filiatie verblijfsobject is ontstaan uit verblijfsobject | BENOEMD OBJECT | |
| *Filiatie verblijfsobject is overgegaan in verblijfsobject | BENOEMD OBJECT | |
| *Kadastraal object bij een verblijfsobject | BENOEMD OBJECT | |
| *Locatieadres van een verblijfsobject | BENOEMD OBJECT | |
| *Verblijfsobject behoort tot WOZ-object | BENOEMD OBJECT | |
| *Verblijfsobject is onderdeel van pand | VERBLIJFSOBJECT | n:m-relatie (in de BGR) i.p.v. een n:1-relatie (in het GFO-BG). |
| Aan/uitbouw | - | |
| Aantal ruimten | - | |
| Bebouwde terreinoppervlakte | - | |
| Bouwjaar | PAND | |
| Bouwjaarklasse | - | |
| Bouwkundige bestemming actueel | GEBOUWD OBJECT | |
| Bouwkundige bestemming oorspronkelijk | - | |
| Bouwtechnische kwaliteitsaanduiding | - | |
| Bruto inhoud | GEBOUWD OBJECT | |
| Bruto vloeroppervlak | - | |
| Centroïd x-coördinaat verblijfsobject | GEBOUWD OBJECT | |
| Centroïd y-coördinaat verblijfsobject | GEBOUWD OBJECT | |
| Centroïd z-coördinaat verblijfsobject | - | |
| Datum aanvang bouw | PAND | Metagegeven van Pandstatus |
| Datum bouw gereed | PAND | Metagegeven van Pandstatus |
| Datum sloop | PAND | Metagegeven van Pandstatus |
| Gemiddelde breedte verblijfsobject | - | |
| Gemiddelde hoogte verblijfsobject | - | |
| Gemiddelde lengte verblijfsobject | - | |
| Hoogste bouwlaag verblijfsobject | VERBLIJFSOBJECT | |
| Laagste bouwlaag verblijfsobject | VERBLIJFSOBJECT | |
| Lifttype | - | |
| Monumentaanduiding | - | |
| Onbebouwde terreinoppervlakte | - | |
| Onderhoudstoestand | - | |
| Renovatiejaar | - | |
| Verblijfsobjectnummer | BENOEMD OBJECT | |
| Verblijfsobjecttype | VERBLIJFSOBJECT | Betreft het gegeventype Gebruiksdoel in de BGR. |
| **Verblijfstitel** | - | Overeenkomstig de GBA niet separaat gemodelleerd. |
| *Verblijfstitel van een natuurlijk persoon | INGEZETENE | |
| Aanduiding verblijfstitel | INGEZETENE | |
| Einddatum verblijfstitel | INGEZETENE | |
| Ingangsdatum verblijfstitel | INGEZETENE | |
| Verblijfstitelomschrijving | INGEZETENE | |
| **Wijk** | WIJK | |
| *Buurt in een wijk | WIJK | |
| *Wijk bij een locatieadres | BENOEMD OBJECT | Relatie loopt via BUURT. |
| *Wijk in een gemeente | WIJK | |
| Einddatum wijk | WIJK | |
| Ingangsdatum wijk | WIJK | |
| Wijkcode | WIJK | |
| Wijknaam | WIJK | |
| **Woonobject** | VERBLIJFSOBJECT | |
| Aantal woonlagen | - | |
| Aantal woonvertrekken | - | |
| Bereikbaarheid hoofdwoonvertrek | - | |
| Binnenwerkse kernoppervlakte | - | |
| Soort woonobject | - | |
| Woonoppervlakte | - | |
| **WOZ-object** | WOZ-OBJECT | |
| *Eigenaar | WOZ-BELANG | |
| *Gebruiker | WOZ-BELANG | |
| *Hoofdadres van een WOZ-object | WOZ-OBJECT | |
| *Huishouden is gehuisvest in WOZ-object | - | Gemodelleerd naar VERBLIJFSOBJECT. |
| *Kadastraal object bij een WOZ-object | WOZ-OBJECT | |
| *Nevenadres van een WOZ-object | - | |
| *Overig bouwwerk behoort tot WOZ-object | WOZ-OBJECT | Relatie naar OVERIG GEBOUWD OBJECT via WOZ-DEELOBJECT |
| *Verblijfsobject behoort tot WOZ-object | WOZ-OBJECT | Via WOZ-DEELOBJECT |
| Activiteit feitelijk | - | |
| Huurprijs | - | |
| Huurprijs (euro) | - | |
| Peildatum huurprijs | - | |
| Vastgestelde waarde | - | |
| Vastgestelde waarde (euro) | WOZ-WAARDE | |
| Waardepeildatum | WOZ-WAARDE | |
| WOZ-objectnummer | WOZ-OBJECT | |
| **Zakelijk recht** | ZAKELIJK RECHT | |
| *Code van een zakelijk recht | ZAKELIJK RECHT | |
| *Subject heeft zakelijk recht | ZAKELIJK RECHT | |
| *Zakelijk recht rust op kadastraal object | ZAKELIJK RECHT | |
| Einddatum zakelijk recht | ZAKELIJK RECHT | |
| Indicatie zakelijk recht met meer zaken verkregen | KADASTRALE ONROERENDE ZAAK | |
| Ingangsdatum zakelijk recht | ZAKELIJK RECHT | |
| Koopjaar zakelijk recht | - | |
| Koopsom zakelijk recht | - | |
| Koopsom zakelijk recht (euro) | KADASTRALE ONROERENDE ZAAK | |
| Noemer aandeel zakelijk recht | ZAKELIJK RECHT | |
| Teller aandeel zakelijk recht | ZAKELIJK RECHT | |
