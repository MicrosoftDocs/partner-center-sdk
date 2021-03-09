---
title: Partner Center supported languages and locales
description: List of ISO2 and ISO3 supported locales for Partner Center.
ms.date: 12/03/2018
ms.service: partner-dashboard
ms.subservice:  partnercenter-sdk
author: cychua
ms.author: cychua
---

# Partner Center supported languages and locales

**Applies To**

- Partner Center
- Partner Center operated by 21Vianet
- Partner Center for Microsoft Cloud Germany
- Partner Center for Microsoft Cloud for US Government

Some Partner Center APIs require a value indicating a locale, country or region. For example, the [Partner Center REST header](headers.md) X-Locale requires a value often in the format "language-country" ("en-US" indicates "English - United States").

In the Partner Center managed APIs, the [CountryValidationRules/dotnet/api/microsoft.store.partnercenter.models.countryvalidationrules.countryvalidationrules) class and the [OfferCategory.Locale/dotnet/api/microsoft.store.partnercenter.models.offers.offercategory.locale), [ServiceRequest.CountryCode/dotnet/api/microsoft.store.partnercenter.models.servicerequests.servicerequest.countrycode), or [CustomerBillingProfile.Culture/dotnet/api/microsoft.store.partnercenter.models.customers.customerbillingprofile.culture) properties require string values that indicate a language or country/region (in the form of an ISO2 language code or ISO3 country/region code), a locale, or a culture (a language ID combined with a country/region code).

The following table lists the cultures and International Standards Organization (ISO) country codes that are supported in the Partner Center APIs.

| Country/Region                           | ISO Alpha 2 Country Code | ISO Alpha 3 Country Code | Supported Culture(s)                  |
|------------------------------------------|--------------------------|--------------------------|---------------------------------------|
| Afghanistan                              | AF                       | AFG                      | ps-AF / en-US                         |
| Åland Islands                            | AX                       | ALA                      | sv-SE / en-US                         |
| Albania                                  | AL                       | ALB                      | sq-AL / en-US                         |
| Algeria                                  | DZ                       | DZA                      | ar-DZ / en-US                         |
| American Samoa                           | AS                       | ASM                      | en-US                                 |
| Andorra                                  | AD                       | AND                      | ca-ES / en-US                         |
| Angola                                   | AO                       | AGO                      | pt-PT / en-US                         |
| Anguilla                                 | AI                       | AIA                      | en-US                                 |
| Antarctica                               | AQ                       | ATA                      | en-US                                 |
| Antigua and Barbuda                      | AG                       | ATG                      | en-US                                 |
| Argentina                                | AR                       | ARG                      | es-AR / en-US                         |
| Armenia                                  | AM                       | ARM                      | hy-AM / en-US                         |
| Aruba                                    | AW                       | ABW                      | nl-NL / en-US                         |
| Australia                                | AU                       | AUS                      | en-AU / en-US                         |
| Austria                                  | AT                       | AUT                      | de-AT / en-US                         |
| Azerbaijan                               | AZ                       | AZE                      | az-Latn-AZ / en-US                    |
| Bahamas                                  | BS                       | BHS                      | en-GB / en-US                         |
| Bahrain                                  | BH                       | BHR                      | ar-BH / en-US                         |
| Bangladesh                               | BD                       | BGD                      | bn-BD / en-US                         |
| Barbados                                 | BB                       | BRB                      | en-GB / en-US                         |
| Belarus                                  | BY                       | BLR                      | be-BY / en-US                         |
| Belgium                                  | BE                       | BEL                      | fr-BE / nl-BE / en-US                 |
| Belize                                   | BZ                       | BLZ                      | en-BZ / en-US                         |
| Benin                                    | BJ                       | BEN                      | fr-FR / en-US                         |
| Bermuda                                  | BM                       | BMU                      | en-GB / en-US                         |
| Bhutan                                   | BT                       | BTN                      | en-US                                 |
| Bolivia                                  | BO                       | BOL                      | es-BO / en-US                         |
| Bonaire                                  | BQ                       | BES                      | nl-NL / en-US                         |
| Bosnia and Herzegovina                   | BA                       | BIH                      | bs-Latn-BA / en-US                    |
| Botswana                                 | BW                       | BWA                      | en-GB / en-US                         |
| Bouvet Island                            | BV                       | BVT                      | nb-NO / en-US                         |
| Brazil                                   | BR                       | BRA                      | pt-BR / en-US                         |
| British Indian Ocean Territory           | IO                       | IOT                      | en-US                                 |
| British Virgin Islands                   | VG                       | VGB                      | en-US                                 |
| Brunei                                   | BN                       | BRN                      | ms-BN / en-US                         |
| Bulgaria                                 | BG                       | BGR                      | bg-BG / en-US                         |
| Burkina Faso                             | BF                       | BFA                      | fr-FR / en-US                         |
| Burundi                                  | BI                       | BDI                      | fr-FR / en-US                         |
| Cabo Verde                               | CV                       | CPV                      | pt-CV / en-US                         |
| Cambodia                                 | KH                       | KHM                      | km-KH / en-US                         |
| Cameroon                                 | CM                       | CMR                      | fr-FR / en-US                         |
| Canada                                   | CA                       | CAN                      | fr-CA / en-US                         |
| Cayman Islands                           | KY                       | CYM                      | en-GB / en-US                         |
| Central African Republic                 | CF                       | CAF                      | fr-FR / en-US                         |
| Chad                                     | TD                       | TCD                      | fr-FR / en-US                         |
| Chile                                    | CL                       | CHL                      | es-CL / en-US                         |
| China                                    | CN                       | CHN                      | zh-CN / en-US                         |
| Christmas Island                         | CX                       | CXR                      | en-US                                 |
| Cocos (Keeling) Islands                  | CC                       | CCK                      | en-US                                 |
| Colombia                                 | CO                       | COL                      | es-CO / en-US                         |
| Comoros                                  | KM                       | COM                      | fr-FR / en-US                         |
| Congo                                    | CG                       | COG                      | fr-FR / en-US                         |
| Congo (DRC)                              | CD                       | COD                      | fr-FR / en-US                         |
| Cook Islands                             | CK                       | COK                      | en-US                                 |
| Costa Rica                               | CR                       | CRI                      | es-CR / en-US                         |
| Côte d'Ivoire                            | CI                       | CIV                      | fr-FR / en-US                         |
| Croatia                                  | HR                       | HRV                      | hr-HR / en-US                         |
| Curaçao                                  | CW                       | CUW                      | nl-NL / en-US                         |
| Cyprus                                   | CY                       | CYP                      | el-GR / en-US                         |
| Czechia                                  | CZ                       | CZE                      | cs-CZ / en-US                         |
| Denmark                                  | DK                       | DNK                      | da-DK / en-US                         |
| Djibouti                                 | DJ                       | DJI                      | fr-FR / en-US                         |
| Dominica                                 | DM                       | DMA                      | en-US                                 |
| Dominican Republic                       | DO                       | DOM                      | es-DO / en-US                         |
| Ecuador                                  | EC                       | ECU                      | es-EC / en-US                         |
| Egypt                                    | EG                       | EGY                      | ar-EG / en-US                         |
| El Salvador                              | SV                       | SLV                      | es-SV / en-US                         |
| Equatorial Guinea                        | GQ                       | GNQ                      | es-ES / en-US                         |
| Eritrea                                  | ER                       | ERI                      | ar-SA / en-US                         |
| Estonia                                  | EE                       | EST                      | et-EE / en-US                         |
| eSwatini                                 | SZ                       | SWZ                      | en-US                                 |
| Ethiopia                                 | ET                       | ETH                      | am-ET / en-US                         |
| Falkland Islands                         | FK                       | FLK                      | en-US                                 |
| Faroe Islands                            | FO                       | FRO                      | fo-FO / en-US                         |
| Fiji                                     | FJ                       | FJI                      | en-GB / en-US                         |
| Finland                                  | FI                       | FIN                      | fi-FI / sv-FI / en-US                 |
| France                                   | FR                       | FRA                      | fr-FR / en-US                         |
| French Guiana                            | GF                       | GUF                      | fr-FR / en-US                         |
| French Polynesia                         | PF                       | PYF                      | fr-FR / en-US                         |
| French Southern Territories              | TF                       | ATF                      | fr-FR / en-US                         |
| Gabon                                    | GA                       | GAB                      | fr-FR / en-US                         |
| Gambia                                   | GM                       | GMB                      | en-US                                 |
| Georgia                                  | GE                       | GEO                      | ka-GE / en-US                         |
| Germany                                  | DE                       | DEU                      | de-DE / en-US                         |
| Ghana                                    | GH                       | GHA                      | en-GB / en-US                         |
| Gibraltar                                | GI                       | GIB                      | en-US                                 |
| Greece                                   | GR                       | GRC                      | el-GR / en-US                         |
| Greenland                                | GL                       | GRL                      | da-DK / en-US                         |
| Grenada                                  | GD                       | GRD                      | en-US                                 |
| Guadeloupe                               | GP                       | GLP                      | fr-FR / en-US                         |
| Guam                                     | GU                       | GUM                      | en-US                                 |
| Guatemala                                | GT                       | GTM                      | es-GT / en-US                         |
| Guernsey                                 | GG                       | GGY                      | en-US                                 |
| Guinea                                   | GN                       | GIN                      | fr-FR / en-US                         |
| Guinea-Bissau                            | GW                       | GNB                      | pt-PT / en-US                         |
| Guyana                                   | GY                       | GUY                      | en-US                                 |
| Haiti                                    | HT                       | HTI                      | fr-FR / en-US                         |
| Heard Island and McDonald Islands        | HM                       | HMD                      | en-US                                 |
| Honduras                                 | HN                       | HND                      | es-HN / en-US                         |
| Hong Kong SAR                            | HK                       | HKG                      | zh-HK / en-US                         |
| Hungary                                  | HU                       | HUN                      | hu-HU / en-US                         |
| Iceland                                  | IS                       | ISL                      | is-IS / en-US                         |
| India                                    | IN                       | IND                      | en-IN / hi-IN / en-US                 |
| Indonesia                                | ID                       | IDN                      | id-ID / en-US                         |
| Iraq                                     | IQ                       | IRQ                      | ar-IQ / en-US                         |
| Ireland                                  | IE                       | IRL                      | en-IE / en-US                         |
| Isle of Man                              | IM                       | IMN                      | en-US                                 |
| Israel                                   | IL                       | ISR                      | he-IL / en-US                         |
| Italy                                    | IT                       | ITA                      | it-IT / en-US                         |
| Jamaica                                  | JM                       | JAM                      | en-JM / en-US                         |
| Jan Mayen                                | XJ                       | XJA                      | nb-NO / en-US                         |
| Japan                                    | JP                       | JPN                      | ja-JP / en-US                         |
| Jersey                                   | JE                       | JEY                      | en-US                                 |
| Jordan                                   | JO                       | JOR                      | ar-JO / en-US                         |
| Kazakhstan                               | KZ                       | KAZ                      | kk-KZ / en-US                         |
| Kenya                                    | KE                       | KEN                      | sw-KE / en-US                         |
| Kiribati                                 | KI                       | KIR                      | en-US                                 |
| Korea                                    | KR                       | KOR                      | ko-KR / en-US                         |
| Kosovo                                   | XK                       | XKS                      | en-US                                 |
| Kuwait                                   | KW                       | KWT                      | ar-KW / en-US                         |
| Kyrgyzstan                               | KG                       | KGZ                      | ky-KG / en-US                         |
| Laos                                     | LA                       | LAO                      | lo-LA / en-US                         |
| Latvia                                   | LV                       | LVA                      | lv-LV / en-US                         |
| Lebanon                                  | LB                       | LBN                      | ar-LB / en-US                         |
| Lesotho                                  | LS                       | LSO                      | en-US                                 |
| Liberia                                  | LR                       | LBR                      | en-US                                 |
| Libya                                    | LY                       | LBY                      | ar-LY / en-US                         |
| Liechtenstein                            | LI                       | LIE                      | de-LI / en-US                         |
| Lithuania                                | LT                       | LTU                      | lt-LT / en-US                         |
| Luxembourg                               | LU                       | LUX                      | de-LU / fr-LU / en-US                 |
| Macao SAR                                | MO                       | MAC                      | zh-MO / en-US                         |
| Macedonia, FYRO                          | MK                       | MKD                      | mk-MK / en-US                         |
| Madagascar                               | MG                       | MDG                      | fr-FR / en-US                         |
| Malawi                                   | MW                       | MWI                      | en-US                                 |
| Malaysia                                 | MY                       | MYS                      | en-MY / en-US                         |
| Maldives                                 | MV                       | MDV                      | dv-MV / en-US                         |
| Mali                                     | ML                       | MLI                      | fr-FR / en-US                         |
| Malta                                    | MT                       | MLT                      | mt-MT / en-US                         |
| Marshall Islands                         | MH                       | MHL                      | en-US                                 |
| Martinique                               | MQ                       | MTQ                      | fr-FR / en-US                         |
| Mauritania                               | MR                       | MRT                      | ar-SA / en-US                         |
| Mauritius                                | MU                       | MUS                      | en-GB / en-US                         |
| Mayotte                                  | YT                       | MYT                      | fr-FR / en-US                         |
| Mexico                                   | MX                       | MEX                      | es-MX / en-US                         |
| Micronesia                               | FM                       | FSM                      | en-US                                 |
| Moldova                                  | MD                       | MDA                      | ro-RO / en-US                         |
| Monaco                                   | MC                       | MCO                      | fr-MC / en-US                         |
| Mongolia                                 | MN                       | MNG                      | mn-MN / en-US                         |
| Montenegro                               | ME                       | MNE                      | sr-Latn-ME / en-US                    |
| Montserrat                               | MS                       | MSR                      | en-US                                 |
| Morocco                                  | MA                       | MAR                      | ar-MA / en-US                         |
| Mozambique                               | MZ                       | MOZ                      | pt-PT                                 |
| Myanmar                                  | MM                       | MMR                      | en-US                                 |
| Namibia                                  | NA                       | NAM                      | en-GB / en-US                         |
| Nauru                                    | NR                       | NRU                      | en-US                                 |
| Nepal                                    | NP                       | NPL                      | ne-NP / en-US                         |
| Netherlands Antilles                     | AN                       | ANT                      | en-US                                 |
| Netherlands, The                         | NL                       | NLD                      | nl-NL / en-US                         |
| New Caledonia                            | NC                       | NCL                      | fr-FR / en-US                         |
| New Zealand                              | NZ                       | NZL                      | en-NZ / en-US                         |
| Nicaragua                                | NI                       | NIC                      | es-NI / en-US                         |
| Niger                                    | NE                       | NER                      | fr-FR / en-US                         |
| Nigeria                                  | NG                       | NGA                      | ha-Latn-NG / en-US                    |
| Niue                                     | NU                       | NIU                      | en-US                                 |
| Norfolk Island                           | NF                       | NFK                      | en-US                                 |
| Northern Mariana Islands                 | MP                       | MNP                      | en-US                                 |
| Norway                                   | NO                       | NOR                      | nb-NO / en-US                         |
| Oman                                     | OM                       | OMN                      | ar-OM / en-US                         |
| Pakistan                                 | PK                       | PAK                      | ur-PK / en-US                         |
| Palau                                    | PW                       | PLW                      | en-US                                 |
| Palestinian Authority                    | PS                       | PSE                      | ar-SA / en-US                         |
| Panama                                   | PA                       | PAN                      | es-PA / en-US                         |
| Papua New Guinea                         | PG                       | PNG                      | en-US                                 |
| Paraguay                                 | PY                       | PRY                      | es-PY / en-US                         |
| Peru                                     | PE                       | PER                      | es-PE / en-US                         |
| Philippines                              | PH                       | PHL                      | en-PH / en-US                         |
| Pitcairn Islands                         | PN                       | PCN                      | en-US                                 |
| Poland                                   | PL                       | POL                      | pl-PL / en-US                         |
| Portugal                                 | PT                       | PRT                      | pt-PT / en-US                         |
| Puerto Rico                              | PR                       | PRI                      | es-PR / en-US                         |
| Qatar                                    | QA                       | QAT                      | ar-QA / en-US                         |
| Réunion                                  | RE                       | REU                      | fr-FR / en-US                         |
| Romania                                  | RO                       | ROU                      | ro-RO / en-US                         |
| Russia                                   | RU                       | RUS                      | ru-RU / en-US                         |
| Rwanda                                   | RW                       | RWA                      | rw-RW / en-US                         |
| Saba                                     | XS                       | XSA                      | nl-NL / en-US                         |
| Saint Kitts and Nevis                    | KN                       | KNA                      | en-GB / en-US                         |
| Saint Lucia                              | LC                       | LCA                      | en-US                                 |
| Saint Martin                             | MF                       | MAF                      | fr-FR / en-US                         |
| Saint Pierre and Miquelon                | PM                       | SPM                      | fr-FR / en-US                         |
| Saint Vincent and the Grenadines         | VC                       | VCT                      | en-US                                 |
| Saint-Barthélemy                         | BL                       | BLM                      | fr-FR / en-US                         |
| Samoa                                    | WS                       | WSM                      | en-US                                 |
| San Marino                               | SM                       | SMR                      | it-IT / en-US                         |
| São Tomé and Príncipe                    | ST                       | STP                      | pt-PT / en-US                         |
| Saudi Arabia                             | SA                       | SAU                      | ar-SA / en-US                         |
| Senegal                                  | SN                       | SEN                      | wo-SN / en-US                         |
| Serbia                                   | RS                       | SRB                      | sr-Latn-RS / sr-Cyrl-RS / en-US       |
| Seychelles                               | SC                       | SYC                      | en-US                                 |
| Sierra Leone                             | SL                       | SLE                      | en-US                                 |
| Singapore                                | SG                       | SGP                      | en-SG / zh-SG / en-US                 |
| Sint Eustatius                           | XE                       | XSE                      | nl-NL / en-US                         |
| Sint Maarten                             | SX                       | SXM                      | en-US                                 |
| Slovakia                                 | SK                       | SVK                      | sk-SK / en-US                         |
| Slovenia                                 | SI                       | SVN                      | sl-SI / en-US                         |
| Solomon Islands                          | SB                       | SLB                      | en-US                                 |
| Somalia                                  | SO                       | SOM                      | ar-SA / en-US                         |
| South Africa                             | ZA                       | ZAF                      | en-ZA / en-US                         |
| South Georgia and South Sandwich Islands | GS                       | SGS                      | en-US                                 |
| South Sudan                              | SS                       | SSD                      | en-US                                 |
| Spain                                    | ES                       | ESP                      | es-ES / ca-ES / eu-ES / gl-ES / en-US |
| Sri Lanka                                | LK                       | LKA                      | si-LK / en-US                         |
| St Helena, Ascension, Tristan da Cunha   | SH                       | SHN                      | en-US                                 |
| Suriname                                 | SR                       | SUR                      | nl-NL                                 |
| Svalbard                                 | SJ                       | SJM                      | nb-NO / en-US                         |
| Sweden                                   | SE                       | SWE                      | sv-SE / en-US                         |
| Switzerland                              | CH                       | CHE                      | de-CH / fr-CH / it-CH / en-US         |
| Taiwan                                   | TW                       | TWN                      | zh-TW / en-US                         |
| Tajikistan                               | TJ                       | TJK                      | tg-Cyrl-TJ / en-US                    |
| Tanzania                                 | TZ                       | TZA                      | en-GB / en-US                         |
| Thailand                                 | TH                       | THA                      | th-TH / en-US                         |
| Timor-Leste                              | TL                       | TLS                      | pt-PT / en-US                         |
| Togo                                     | TG                       | TGO                      | fr-FR / en-US                         |
| Tokelau                                  | TK                       | TKL                      | en-US                                 |
| Tonga                                    | TO                       | TON                      | en-US                                 |
| Trinidad and Tobago                      | TT                       | TTO                      | en-TT / en-US                         |
| Tunisia                                  | TN                       | TUN                      | ar-TN / en-US                         |
| Turkey                                   | TR                       | TUR                      | tr-TR / en-US                         |
| Turkmenistan                             | TM                       | TKM                      | tk-TM / en-US                         |
| Turks and Caicos Islands                 | TC                       | TCA                      | en-US                                 |
| Tuvalu                                   | TV                       | TUV                      | en-US                                 |
| Uganda                                   | UG                       | UGA                      | en-GB / en-US                         |
| Ukraine                                  | UA                       | UKR                      | uk-UA / en-US                         |
| United Arab Emirates                     | AE                       | ARE                      | ar-AE / en-US                         |
| United Kingdom                           | GB                       | GBR                      | en-GB / en-US                         |
| U.S. Outlying Islands                    | UM                       | UMI                      | en-US                                 |
| U.S. Virgin Islands                      | VI                       | VIR                      | en-US                                 |
| United States                            | US                       | USA                      | en-US / es-US                         |
| Uruguay                                  | UY                       | URY                      | es-UY / en-US                         |
| Uzbekistan                               | UZ                       | UZB                      | uz-Latn-UZ / en-US                    |
| Vanuatu                                  | VU                       | VUT                      | en-US                                 |
| Vatican City                             | VA                       | VAT                      | it-IT / en-US                         |
| Venezuela                                | VE                       | VEN                      | es-VE / en-US                         |
| Vietnam                                  | VN                       | VNM                      | vi-VN / en-US                         |
| Wallis and Futuna                        | WF                       | WLF                      | fr-FR / en-US                         |
| Yemen                                    | YE                       | YEM                      | ar-YE / en-US                         |
| Zambia                                   | ZM                       | ZMB                      | en-GB / en-US                         |
| Zimbabwe                                 | ZW                       | ZWE                      | en-ZW / en-US                         |

