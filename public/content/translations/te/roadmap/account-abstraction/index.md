---
title: అకౌంట్ సారాంశం
description: వినియోగదారు ఖాతాలను సులభతరం చేయడానికి మరియు సురక్షితంగా చేయడానికి Ethereum యొక్క ప్రణాళికల యొక్క అవలోకనం
lang: te
summaryPoints:
  - ఖాతా సంగ్రహణ స్మార్ట్ కాంట్రాక్ట్ వాలెట్‌లను నిర్మించడాన్ని సులభతరం చేస్తుంది
  - స్మార్ట్ కాంట్రాక్ట్ వాలెట్‌లు Ethereum ఖాతాలకు యాక్సెస్‌ను నిర్వహించడం చాలా సులభతరం చేస్తాయి
  - కోల్పోయిన మరియు బహిర్గతమైన కీలను బహుళ బ్యాకప్‌లను ఉపయోగించి తిరిగి పొందవచ్చు
---

# అకౌంట్ సారాంశం {#account-abstraction}

వినియోగదారులు **[బాహ్య యాజమాన్య ఖాతాలను (EOAలు)](/glossary/#eoa)** ఉపయోగించి Ethereumతో పరస్పర చర్య చేస్తారు. లావాదేవీని ప్రారంభించడానికి లేదా స్మార్ట్ ఒప్పందాన్ని అమలు చేయడానికి ఇది ఏకైక మార్గం. వినియోగదారులు Ethereumతో ఎలా పరస్పర చర్య చేయగలరో ఇది పరిమితం చేస్తుంది. ఉదాహరణకు, లావాదేవీల బ్యాచ్‌లను చేయడం కష్టతరం చేస్తుంది మరియు వినియోగదారులు గ్యాస్‌ను కవర్ చేయడానికి ఎల్లప్పుడూ ETH బ్యాలెన్స్‌ను ఉంచుకోవాల్సిన అవసరం ఉంది.

ఖాతా సంగ్రహణ అనేది వినియోగదారులను వారి ఖాతాలోకి మరింత భద్రత మరియు మెరుగైన వినియోగదారు అనుభవాలను అనువైన ప్రోగ్రామ్ చేయడానికి అనుమతించడం ద్వారా ఈ సమస్యలను పరిష్కరించడానికి ఒక మార్గం. [EOAలను అప్‌గ్రేడ్ చేయడం](https://eips.ethereum.org/EIPS/eip-3074) ద్వారా ఇది జరుగుతుంది, తద్వారా వాటిని స్మార్ట్ కాంట్రాక్టుల ద్వారా నియంత్రించవచ్చు లేదా [స్మార్ట్ కాంట్రాక్టులను అప్‌గ్రేడ్ చేయడం](https://eips.ethereum.org/EIPS/eip-2938) ద్వారా లావాదేవీలను ప్రారంభించవచ్చు. ఈ ఎంపికలు రెండింటికీ Ethereum ప్రోటోకాల్‌కు మార్పులు అవసరం. ఇప్పటికే ఉన్న ప్రోటోకాల్‌కు సమాంతరంగా అమలు చేయడానికి [రెండవ, ప్రత్యేక లావాదేవీ వ్యవస్థ](https://eips.ethereum.org/EIPS/eip-4337)ను జోడించడంతోపాటు మూడవ మార్గం కూడా ఉంది. మార్గంతో సంబంధం లేకుండా, ఫలితం స్మార్ట్ కాంట్రాక్ట్ వాలెట్ల ద్వారా Ethereumకు యాక్సెస్, ఇప్పటికే ఉన్న ప్రోటోకాల్‌లో భాగంగా లేదా యాడ్-ఆన్ లావాదేవీ నెట్‌వర్క్ ద్వారా స్థానికంగా మద్దతు ఇవ్వబడుతుంది.

స్మార్ట్ కాంట్రాక్ట్ వాలెట్‌లు వినియోగదారు కోసం అనేక ప్రయోజనాలను అన్‌లాక్ చేస్తాయి, వీటితో సహా:

- మీ స్వంత సౌకర్యవంతమైన భద్రతా నియమాలను నిర్వచించడం
- మీరు కీలను పోగొట్టుకుంటే మీ ఖాతాను తిరిగి పొందడం
- విశ్వసనీయ పరికరాలు లేదా వ్యక్తులలో మీ ఖాతా భద్రతను భాగస్వామ్యం చేయడం
- వేరొకరి గ్యాస్ చెల్లించడం లేదా మరొకరు మీది చెల్లించేలా చేయడం
- బ్యాచ్ లావాదేవీలు కలిసి (ఉదా. ఒక స్వాప్‌ను ఆమోదించడం మరియు అమలు చేయడం)
- వినియోగదారు అనుభవాలను ఆవిష్కరించడానికి dapps మరియు వాలెట్ డెవలపర్‌లకు మరిన్ని అవకాశాలు

ఈ ప్రయోజనాలకు ఈరోజు స్థానికంగా మద్దతు లేదు ఎందుకంటే బాహ్యంగా స్వంతమైన ఖాతాలు ([EOAలు](/glossary/#eoa)) మాత్రమే లావాదేవీలను ప్రారంభించగలవు. EOAలు కేవలం పబ్లిక్-ప్రైవేట్ కీ జతలు. వారు ఇలా పని చేస్తారు:

- మీరు ప్రైవేట్ కీని కలిగి ఉంటే, మీరు Ethereum వర్చువల్ మెషిన్ (EVM) నియమాలకు లోబడి _ఏదైనా_ చేయవచ్చు
- మీరు ప్రైవేట్ కీని కలిగి లేకుంటే మీరు _ఏమీ చేయలేరు_.

మీరు మీ కీలను పోగొట్టుకుంటే వాటిని తిరిగి పొందలేరు మరియు దొంగిలించబడిన కీలు దొంగలకు ఖాతాలోని అన్ని నిధులకు తక్షణ ప్రాప్యతను అందిస్తాయి.

స్మార్ట్ కాంట్రాక్ట్ వాలెట్‌లు ఈ సమస్యలకు పరిష్కారం, కానీ ఈరోజు వాటిని ప్రోగ్రామ్ చేయడం కష్టంగా ఉంది, ఎందుకంటే చివరికి, వారు అమలు చేసే ఏదైనా లాజిక్‌ను Ethereum ద్వారా ప్రాసెస్ చేయడానికి ముందు EOA లావాదేవీల సమితిలోకి అనువదించవలసి ఉంటుంది. ఖాతా సంగ్రహణ స్మార్ట్ కాంట్రాక్టులను స్వయంగా లావాదేవీలను ప్రారంభించడానికి వీలు కల్పిస్తుంది, తద్వారా వినియోగదారు అమలు చేయాలనుకునే ఏదైనా లాజిక్ స్మార్ట్ కాంట్రాక్ట్ వాలెట్‌లోనే కోడ్ చేయబడుతుంది మరియు Ethereumలో అమలు చేయబడుతుంది.

అంతిమంగా, ఖాతా సంగ్రహణ స్మార్ట్ కాంట్రాక్ట్ వాలెట్‌లకు మద్దతును మెరుగుపరుస్తుంది, వాటిని నిర్మించడం సులభం మరియు ఉపయోగించడానికి సురక్షితమైనది. చివరికి, ఖాతా సంగ్రహణతో, వినియోగదారులు అంతర్లీన సాంకేతికత గురించి తెలియకుండా లేదా పట్టించుకోకుండా Ethereum యొక్క అన్ని ప్రయోజనాలను ఆస్వాదించవచ్చు.

## సీడ్ పదబంధాలకు మించి {#beyond-seed-phrases}

సీడ్ పదబంధాల నుండి లెక్కించబడే ప్రైవేట్ కీలను ఉపయోగించి నేటి ఖాతాలు సురక్షితంగా ఉంటాయి. విత్తన పదబంధానికి ప్రాప్యత ఉన్న ఎవరైనా ఖాతాను రక్షించే ప్రైవేట్ కీని సులభంగా కనుగొనవచ్చు మరియు అది రక్షించే అన్ని ఆస్తులకు ప్రాప్యతను పొందవచ్చు. ప్రైవేట్ కీ మరియు విత్తన పదబంధాన్ని పోగొట్టుకుంటే, వాటిని ఎప్పటికీ తిరిగి పొందలేము మరియు వారు నియంత్రించే ఆస్తులు శాశ్వతంగా స్తంభింపజేయబడతాయి. ఈ విత్తన పదబంధాలను భద్రపరచడం అనేది నిపుణులైన వినియోగదారులకు కూడా ఇబ్బందికరంగా ఉంటుంది మరియు వినియోగదారులు స్కామ్‌లకు గురయ్యే అత్యంత సాధారణ మార్గాలలో సీడ్ ఫ్రేజ్ ఫిషింగ్ కూడా ఒకటి.

ఆస్తులను కలిగి ఉండటానికి మరియు లావాదేవీలను ప్రామాణీకరించడానికి స్మార్ట్ ఒప్పందాన్ని ఉపయోగించడం ద్వారా ఖాతా సంగ్రహణ ఈ సమస్యను పరిష్కరిస్తుంది. ఈ స్మార్ట్ కాంట్రాక్టులను అనుకూల లాజిక్‌తో అలంకరించవచ్చు, తద్వారా వాటిని వీలైనంత సురక్షితంగా మరియు వినియోగదారుకు అనుగుణంగా రూపొందించవచ్చు. అంతిమంగా, మీరు ఇప్పటికీ మీ ఖాతాకు యాక్సెస్‌ను నియంత్రించడానికి ప్రైవేట్ కీలను ఉపయోగిస్తున్నారు, కానీ వాటిని నిర్వహించడం సులభతరం మరియు సురక్షితమైన భద్రతా నెట్‌లతో.

ఉదాహరణకు, బ్యాకప్ కీలను వాలెట్‌కు జోడించవచ్చు, తద్వారా మీరు మీ ప్రధాన కీని పోగొట్టుకున్నా లేదా అనుకోకుండా బహిర్గతం చేసినా, బ్యాకప్ కీల నుండి అనుమతితో దాన్ని కొత్త, సురక్షితమైన దానితో భర్తీ చేయవచ్చు. మీరు ఈ ప్రతి కీని వేరే విధంగా భద్రపరచవచ్చు లేదా విశ్వసనీయ సంరక్షకుల మధ్య వాటిని విభజించవచ్చు. ఇది మీ నిధులపై పూర్తి నియంత్రణను పొందేందుకు దొంగకు చాలా కష్టతరం చేస్తుంది. అదేవిధంగా, మీ ప్రధాన కీ రాజీపడితే ప్రభావాన్ని తగ్గించడానికి మీరు వాలెట్‌కు నియమాలను జోడించవచ్చు, ఉదాహరణకు, తక్కువ-విలువ లావాదేవీలను ఒకే సంతకం ద్వారా ధృవీకరించడానికి మీరు అనుమతించవచ్చు, అయితే అధిక-విలువ లావాదేవీలకు బహుళ ప్రామాణీకరించబడిన సంతకందారుల నుండి ఆమోదం అవసరం. దొంగలను అడ్డుకోవడంలో స్మార్ట్ కాంట్రాక్ట్ వాలెట్‌లు మీకు సహాయపడగల ఇతర మార్గాలు ఉన్నాయి, ఉదాహరణకు, విశ్వసనీయ చిరునామాకు లేదా మీ ముందుగా ఆమోదించబడిన అనేక కీల ద్వారా ధృవీకరించబడినట్లయితే తప్ప, ప్రతి లావాదేవీని బ్లాక్ చేయడానికి అనుమతి జాబితాను ఉపయోగించవచ్చు.

### స్మార్ట్ కాంట్రాక్ట్ వాలెట్‌లో నిర్మించబడే భద్రతా లాజిక్ ఉదాహరణలు:

- స్మార్ట్ కాంట్రాక్ట్ వాలెట్‌లో నిర్మించబడే భద్రతా లాజిక్ ఉదాహరణలు: ఆ తర్వాత ఒప్పందాన్ని కాన్ఫిగర్ చేయవచ్చు, తద్వారా కొంత ప్రీసెట్ విలువ కంటే ఎక్కువ లావాదేవీలకు విశ్వసనీయ పక్షాల నిర్దిష్ట నిష్పత్తి (ఉదా. 3/5) నుండి అనుమతి అవసరం. ఉదాహరణకు, అధిక-విలువ లావాదేవీలకు మొబైల్ పరికరం మరియు హార్డ్‌వేర్ వాలెట్ రెండింటి నుండి ఆమోదం అవసరం కావచ్చు లేదా విశ్వసనీయ కుటుంబ సభ్యులకు పంపిణీ చేయబడిన ఖాతాల నుండి సంతకాలు అవసరం కావచ్చు.
- **ఖాతా స్తంభింపజేయడం**: పరికరం పోయినా లేదా రాజీపడినా, వినియోగదారు ఆస్తులను రక్షించడం ద్వారా ఖాతా మరొక అధీకృత పరికరం నుండి లాక్ చేయబడవచ్చు.
- **ఖాతా పునరుద్ధరణ**: పరికరాన్ని పోగొట్టుకున్నారా లేదా పాస్‌వర్డ్ మర్చిపోయారా? ప్రస్తుత నమూనాలో, మీ ఆస్తులు శాశ్వతంగా స్తంభింపజేయవచ్చని దీని అర్థం: ఉదాహరణకు, అధిక-విలువ లావాదేవీలకు మొబైల్ పరికరం మరియు హార్డ్‌వేర్ వాలెట్ రెండింటి నుండి ఆమోదం అవసరం కావచ్చు లేదా విశ్వసనీయ కుటుంబ సభ్యులకు పంపిణీ చేయబడిన ఖాతాల నుండి సంతకాలు అవసరం కావచ్చు:
- లావాదేవీ పరిమితులను సెట్ చేయండి: ఒక రోజు/వారం/నెలలో ఖాతా నుండి ఎంత విలువను బదిలీ చేయవచ్చో రోజువారీ థ్రెషోల్డ్‌లను పేర్కొనండి: దాడి చేసే వ్యక్తి మీ ఖాతాకు ప్రాప్యతను పొందినట్లయితే, వారు ఒకేసారి అన్నింటినీ తీసివేయలేరు మరియు యాక్సెస్‌ను స్తంభింపజేసేందుకు మరియు రీసెట్ చేయడానికి మీకు అవకాశాలు ఉంటాయి:
- **అనుమతి జాబితాలను సృష్టించండి**: మీరు సురక్షితంగా ఉన్నారని తెలిసిన నిర్దిష్ట చిరునామాలకు మాత్రమే లావాదేవీలను అనుమతించండి. దీనర్థం _ఒకవేళ_ మీ ప్రైవేట్ కీ దొంగిలించబడినప్పటికీ, దాడి చేసే వ్యక్తి మీ జాబితాలోని గమ్యస్థాన ఖాతాలకు మాత్రమే నిధులను పంపగలడు. ఈ అనుమతి జాబితాలకు వాటిని మార్చడానికి బహుళ సంతకాలు అవసరమవుతాయి, తద్వారా దాడి చేసేవారు మీ బ్యాకప్ కీలలో చాలా వాటికి యాక్సెస్ కలిగి ఉంటే తప్ప వారి స్వంత చిరునామాను జాబితాకు జోడించలేరు.

## మెరుగైన యూజర్ అనుభవం {#better-user-experience}

ఖాతా సంగ్రహణ **మెరుగైన మొత్తం వినియోగదారు అనుభవాన్ని** అలాగే **మెరుగైన భద్రతను** అనుమతిస్తుంది ఎందుకంటే ఇది ప్రోటోకాల్ స్థాయిలో స్మార్ట్ కాంట్రాక్ట్ వాలెట్‌లకు మద్దతును జోడిస్తుంది. దీనికి అతి ముఖ్యమైన కారణం ఏమిటంటే, ఇది స్మార్ట్ కాంట్రాక్టులు, వాలెట్‌లు మరియు అప్లికేషన్‌ల డెవలపర్‌లకు వినియోగదారు అనుభవాన్ని ఇంకా ఊహించలేని మార్గాల్లో ఆవిష్కరించడానికి మరింత స్వేచ్ఛను అందిస్తుంది. ఖాతా సంగ్రహణతో పాటు వచ్చే కొన్ని స్పష్టమైన మెరుగుదలలు వేగం మరియు సామర్థ్యం కోసం లావాదేవీల బండిల్‌ను కలిగి ఉంటాయి. ఉదాహరణకు, ఒక సాధారణ స్వాప్ అనేది ఒక-క్లిక్ ఆపరేషన్ అయి ఉండాలి, కానీ ఈ రోజు స్వాప్ అమలు చేయబడే ముందు వ్యక్తిగత టోకెన్‌ల ఖర్చును ఆమోదించడానికి బహుళ లావాదేవీలపై సంతకం చేయాల్సి ఉంటుంది. ఖాతా సంగ్రహణ లావాదేవీ బండిలింగ్‌ను అనుమతించడం ద్వారా ఆ ఘర్షణను తొలగిస్తుంది. ఇంకా, బండిల్ చేయబడిన లావాదేవీ ప్రతి లావాదేవీకి అవసరమైన టోకెన్‌ల యొక్క సరైన విలువను ఖచ్చితంగా ఆమోదించగలదు మరియు అదనపు భద్రతను అందించడం ద్వారా లావాదేవీ పూర్తయిన తర్వాత ఆమోదాలను ఉపసంహరించుకోవచ్చు.

ఖాతా సంగ్రహణతో గ్యాస్ నిర్వహణ కూడా చాలా మెరుగుపడింది. అప్లికేషన్‌లు తమ వినియోగదారుల గ్యాస్ రుసుములను చెల్లించడం మాత్రమే కాకుండా, ETH కాకుండా ఇతర టోకెన్‌లలో గ్యాస్ ఫీజులను చెల్లించవచ్చు, నిధుల లావాదేవీల కోసం ETH బ్యాలెన్స్‌ను నిర్వహించకుండా వినియోగదారులను విముక్తి చేస్తుంది. ఒప్పందం లోపల ETH కోసం వినియోగదారు టోకెన్‌లను మార్చుకోవడం ద్వారా మరియు గ్యాస్ కోసం చెల్లించడానికి ETHని ఉపయోగించడం ద్వారా ఇది పని చేస్తుంది.

<ExpandableCard title="గ్యాస్‌తో ఖాతా సంగ్రహణ ఎలా సహాయపడుతుంది?" eventCategory="/roadmap/account-abstraction" eventName="clicked how can account abstraction help with gas?">

Ethereum వినియోగదారులకు గ్యాస్ మేనేజ్‌మెంట్ ప్రాథమిక ఘర్షణలలో ఒకటి, ప్రధానంగా లావాదేవీల కోసం చెల్లించడానికి ఉపయోగించే ఏకైక ఆస్తి ETH. మీరు USDC బ్యాలెన్స్‌తో కూడిన వాలెట్‌ని కలిగి ఉన్నారని ఊహించుకోండి, కానీ ETH లేదు. మీరు గ్యాస్ చెల్లించలేరు కాబట్టి మీరు ఆ USDC టోకెన్‌లను తరలించలేరు లేదా మార్పిడి చేయలేరు. మీరు ETH కోసం USDCని కూడా మార్చుకోలేరు, ఎందుకంటే దానికే గ్యాస్ ఖర్చవుతుంది. సమస్యను పరిష్కరించడానికి మీరు ఎక్స్ఛేంజ్ లేదా మరొక చిరునామా నుండి మీ ఖాతాకు మరింత ETHని పంపాలి. స్మార్ట్ కాంట్రాక్ట్ వాలెట్‌లతో, మీరు మీ ఖాతాను విడిపించేందుకు బదులుగా USDCలో గ్యాస్ చెల్లించవచ్చు. మీరు ఇకపై మీ అన్ని ఖాతాలలో ETH బ్యాలెన్స్ ఉంచాల్సిన అవసరం లేదు.

ఖాతా సంగ్రహణ కూడా dapp డెవలపర్‌లు గ్యాస్ మేనేజ్‌మెంట్‌తో సృజనాత్మకంగా ఉండటానికి అనుమతిస్తుంది. ఉదాహరణకు, మీరు అపరిమిత లావాదేవీల కోసం ప్రతి నెలా మీకు ఇష్టమైన DEXకి నిర్ణీత రుసుమును చెల్లించడం ప్రారంభించవచ్చు. Dapps వారి ప్లాట్‌ఫారమ్‌ను ఉపయోగించినందుకు రివార్డ్‌గా లేదా ఆన్‌బోర్డింగ్ ఆఫర్‌గా మీ తరపున మీ గ్యాస్ ఫీజు మొత్తాన్ని చెల్లించడానికి ఆఫర్ చేయవచ్చు. ప్రోటోకాల్ స్థాయిలో స్మార్ట్ కాంట్రాక్ట్ వాలెట్‌లకు మద్దతు ఇచ్చినప్పుడు డెవలపర్‌లు గ్యాస్‌పై ఆవిష్కరణలు చేయడం చాలా సులభం అవుతుంది.

</ExpandableCard>

విశ్వసనీయ సెషన్‌లు వినియోగదారు అనుభవాల కోసం, ప్రత్యేకించి గేమింగ్ వంటి అప్లికేషన్‌ల కోసం సంభావ్యంగా రూపాంతరం చెందుతాయి, ఇక్కడ పెద్ద సంఖ్యలో చిన్న లావాదేవీలకు తక్కువ సమయంలో ఆమోదం అవసరం కావచ్చు. ప్రతి లావాదేవీని వ్యక్తిగతంగా ఆమోదించడం గేమింగ్ అనుభవాన్ని విచ్ఛిన్నం చేస్తుంది, కానీ శాశ్వత ఆమోదం సురక్షితం కాదు. స్మార్ట్ కాంట్రాక్ట్ వాలెట్ నిర్దిష్ట లావాదేవీలను నిర్దిష్ట కాలానికి, నిర్దిష్ట విలువ వరకు లేదా నిర్దిష్ట చిరునామాలకు మాత్రమే ఆమోదించగలదు.

ఖాతా సంగ్రహణతో కొనుగోళ్లు ఎలా మారతాయో పరిశీలించడం కూడా ఆసక్తికరంగా ఉంటుంది. ఈ రోజు, ప్రతి లావాదేవీ సరైన టోకెన్‌తో ముందస్తుగా ఫండ్ చేయబడిన వాలెట్ నుండి ఆమోదించబడాలి మరియు అమలు చేయబడాలి. ఖాతా సంగ్రహణతో, వినియోగదారుడు ఐటెమ్‌లతో "బాస్కెట్"ని నింపి, కాంట్రాక్ట్ ద్వారా నిర్వహించాల్సిన అన్ని లాజిక్‌లతో, వినియోగదారు కాకుండా ఒకేసారి కొనుగోలు చేయడానికి ఒకసారి క్లిక్ చేసే అనుభవం తెలిసిన ఆన్‌లైన్ షాపింగ్ లాగా ఉంటుంది.

ఖాతా సంగ్రహణ ద్వారా వినియోగదారు అనుభవాలను ఎలా సమం చేయవచ్చు అనేదానికి ఇవి కొన్ని ఉదాహరణలు మాత్రమే, కానీ మనం ఇంకా ఊహించనివి చాలా ఉన్నాయి. ఖాతా సంగ్రహణ డెవలపర్‌లను ప్రస్తుత EOAల పరిమితుల నుండి విముక్తి చేస్తుంది, స్వీయ-నిర్ధారణను త్యాగం చేయకుండా web2లోని మంచి అంశాలను web3లోకి తీసుకురావడానికి మరియు సృజనాత్మకంగా కొత్త వినియోగదారు అనుభవాలను హ్యాక్ చేయడానికి వారిని అనుమతిస్తుంది.

## ఖాతా సంగ్రహణ ఎలా అమలు చేయబడుతుంది? {#how-will-aa-be-implemented}

స్మార్ట్ కాంట్రాక్ట్ వాలెట్లు నేడు ఉన్నాయి కానీ వాటిని EVM సపోర్ట్ చేయనందున అమలు చేయడం సవాలుగా ఉంది. బదులుగా, వారు ప్రామాణిక Ethereum లావాదేవీల చుట్టూ సాపేక్షంగా సంక్లిష్టమైన కోడ్‌ను చుట్టడంపై ఆధారపడతారు. Ethereum స్మార్ట్ కాంట్రాక్టులను లావాదేవీలను ప్రారంభించడానికి అనుమతించడం ద్వారా, ఆఫ్-చెయిన్‌కు బదులుగా Ethereum స్మార్ట్ కాంట్రాక్టులలో అవసరమైన లాజిక్‌ను నిర్వహించడం ద్వారా దీన్ని మార్చవచ్చు. స్మార్ట్ కాంట్రాక్టులలో లాజిక్‌ను ఉంచడం వలన Ethereum యొక్క వికేంద్రీకరణ పెరుగుతుంది, ఎందుకంటే ఇది సాధారణ Ethereum లావాదేవీలకు వినియోగదారు సంతకం చేసిన సందేశాలను అనువదించడానికి వాలెట్ డెవలపర్‌లచే నిర్వహించబడే "రిలేయర్‌ల" అవసరాన్ని తొలగిస్తుంది.

<ExpandableCard title="EIP-2771: మెటా-లావాదేవీలను ఉపయోగించి ఖాతా సంగ్రహణ" eventCategory="/roadmap/account-abstract" eventName="clicked EIP-2771: account abstraction using meta-transactions">

EIP-2771 మెటా-లావాదేవీల భావనను పరిచయం చేస్తుంది, ఇది Ethereum ప్రోటోకాల్‌కు మార్పులు చేయకుండా వినియోగదారు గ్యాస్ ఖర్చులను చెల్లించడానికి మూడవ పక్షాలను అనుమతిస్తుంది. వినియోగదారు సంతకం చేసిన లావాదేవీలు `ఫార్వార్డర్` ఒప్పందానికి పంపబడాలనే ఆలోచన ఉంది. ఫార్వార్డర్ అనేది గ్యాస్ రిలేకు పంపే ముందు లావాదేవీలు చెల్లుబాటు అయ్యేవని ధృవీకరించే విశ్వసనీయ సంస్థ. గ్యాస్ చెల్లించాల్సిన అవసరాన్ని నివారించడం ద్వారా ఇది ఆఫ్-చెయిన్ చేయబడుతుంది. గ్యాస్ రిలే లావాదేవీని 'గ్రహీత' ఒప్పందానికి పంపుతుంది, Ethereumలో లావాదేవీని అమలు చేయడానికి అవసరమైన గ్యాస్‌ను చెల్లిస్తుంది. ఫార్వార్డర్` అనేది `గ్రహీత` ద్వారా తెలిసి మరియు విశ్వసించబడినట్లయితే లావాదేవీ అమలు చేయబడుతుంది. ఈ మోడల్ వినియోగదారుల కోసం గ్యాస్‌లెస్ లావాదేవీలను అమలు చేయడానికి డెవలపర్‌లకు సులభతరం చేస్తుంది.

</ExpandableCard>

<ExpandableCard title="EIP-4337: Ethereum ప్రోటోకాల్‌ను మార్చకుండా ఖాతా సంగ్రహణ" eventCategory="/roadmap/account-abstract" eventName="clicked EIP-4337: account abstraction without changing the Ethereum protocol">

EIP-4337 అనేది వికేంద్రీకృత మార్గంలో <em>Ethereum ప్రోటోకాల్‌కు మార్పులు అవసరం లేకుండా</em> స్థానిక స్మార్ట్ కాంట్రాక్ట్ వాలెట్ మద్దతు వైపు మొదటి అడుగు. స్మార్ట్ కాంట్రాక్ట్ వాలెట్‌లకు మద్దతు ఇచ్చేలా ఏకాభిప్రాయ పొరను సవరించడానికి బదులుగా, సాధారణ లావాదేవీ గాసిప్ ప్రోటోకాల్‌కు విడిగా కొత్త సిస్టమ్ జోడించబడింది. ఈ ఉన్నత-స్థాయి సిస్టమ్ <code>UserOperation</code> అనే కొత్త వస్తువు చుట్టూ నిర్మించబడింది, ఇది సంబంధిత సంతకాలతో పాటు వినియోగదారు నుండి చర్యలను ప్యాకేజీ చేస్తుంది. ఈ <code>UserOperation</code> ఆబ్జెక్ట్‌లు ప్రత్యేక మెంపూల్‌లోకి ప్రసారం చేయబడతాయి, ఇక్కడ చెల్లుబాటుదారులు వాటిని "బండిల్ లావాదేవీ"గా సేకరించవచ్చు. బండిల్ లావాదేవీ అనేక వ్యక్తిగత <code>యూజర్ ఆపరేషన్స్</code> క్రమాన్ని సూచిస్తుంది మరియు సాధారణ లావాదేవీ లాగానే Ethereum బ్లాక్‌లలో చేర్చబడుతుంది మరియు ఇదే విధమైన రుసుము-గరిష్ట ఎంపిక మోడల్‌ను ఉపయోగించి వ్యాలిడేటర్‌ల ద్వారా తీసుకోబడుతుంది.

EIP-4337 క్రింద వాలెట్లు పని చేసే విధానం కూడా మారుతుంది. ప్రతి వాలెట్ సాధారణ కానీ సంక్లిష్టమైన భద్రతా తర్కాన్ని తిరిగి అమలు చేయడానికి బదులుగా, ఆ విధులు &quot;ఎంట్రీ పాయింట్&quot;గా పిలువబడే గ్లోబల్ వాలెట్ కాంట్రాక్ట్‌కు అవుట్‌సోర్స్ చేయబడతాయి. ఇది రుసుము చెల్లించడం మరియు EVM కోడ్‌ను అమలు చేయడం వంటి కార్యకలాపాలను నిర్వహిస్తుంది, తద్వారా వాలెట్ డెవలపర్‌లు అద్భుతమైన వినియోగదారు అనుభవాలను అందించడంపై దృష్టి పెట్టగలరు.

<strong>గమనిక</strong> EIP 4337 ఎంట్రీ పాయింట్ కాంట్రాక్ట్ 1 మార్చి 2023న Ethereum Mainnetకు అమలు చేయబడింది. మీరు ఒప్పందాన్ని <a href="https://etherscan.io/address/0x0576a174D229E3cFA37253523E645A78A0C91B57">Etherscan</a>లో చూడవచ్చు.

</ExpandableCard>

<ExpandableCard title="EIP-2938: ఖాతా సంగ్రహణకు మద్దతు ఇవ్వడానికి Ethereum ప్రోటోకాల్‌ను మార్చడం" eventCategory="/roadmap/account-abstract" eventName="clicked EIP-2938: changing the Ethereum protocol to support account abstraction">

<a href="https://eips.ethereum.org/EIPS/eip-2938">EIP-2938</a> మూడు ఫీల్డ్‌లను కలిగి ఉన్న <code>AA_TX_TYPE</code> కొత్త లావాదేవీ రకాన్ని పరిచయం చేయడం ద్వారా Ethereum ప్రోటోకాల్‌ను నవీకరించాలని లక్ష్యంగా పెట్టుకుంది: <code>nonce</code>, <code>టార్గెట్</code> మరియు <code>డేటా</code>, ఇక్కడ <code>నాన్స్</code> అనేది లావాదేవీ కౌంటర్, <code>టార్గెట్</code> అనేది ఎంట్రీ పాయింట్ కాంట్రాక్ట్ చిరునామా మరియు <code>డేటా</code> EVM బైట్‌కోడ్. ఈ లావాదేవీలను అమలు చేయడానికి, EVMకు రెండు కొత్త సూచనలను (ఆప్‌కోడ్‌లుగా పిలుస్తారు) జోడించాలి: <code>NONCE</code> మరియు <code>PAYGAS</code>. <code>NONCE</code> ఆప్‌కోడ్ లావాదేవీల క్రమాన్ని ట్రాక్ చేస్తుంది మరియు <code>PAYGAS</code> ఒప్పందం యొక్క &#39;sబ్యాలెన్స్ నుండి లావాదేవీని అమలు చేయడానికి అవసరమైన గ్యాస్‌ను గణిస్తుంది మరియు ఉపసంహరించుకుంటుంది. ఈ కొత్త ఫీచర్లు Ethereum&#39;s యొక్క ప్రోటోకాల్‌లో అవసరమైన మౌలిక సదుపాయాలు నిర్మించబడినందున స్థానికంగా స్మార్ట్ కాంట్రాక్ట్ వాలెట్‌లకు మద్దతు ఇవ్వడానికి Ethereumని అనుమతిస్తాయి.

EIP-2938 ప్రస్తుతం సక్రియంగా లేదని గమనించండి. సంఘం ప్రస్తుతం EIP-4337కు అనుకూలంగా ఉంది ఎందుకంటే దీనికి ప్రోటోకాల్‌లో మార్పులు అవసరం లేదు.

</ExpandableCard>

<ExpandableCard title="EIP-3074: ఖాతా సంగ్రహణ కోసం బాహ్య యాజమాన్యంలోని ఖాతాలను అప్‌గ్రేడ్ చేయడం" eventCategory="/roadmap/account-abstract" eventName="clicked EIP-3074: upgrading externally-owned accounts for account abstraction">

<a href="https://eips.ethereum.org/EIPS/eip-3074">EIP-3074</a> Ethereum"&#39;" యొక్క బాహ్య-యాజమాన్య ఖాతాలను స్మార్ట్ ఒప్పందానికి నియంత్రణను అప్పగించడానికి అనుమతించడం ద్వారా వాటిని నవీకరించడం లక్ష్యంగా పెట్టుకుంది. స్మార్ట్ కాంట్రాక్ట్ లాజిక్ EOA నుండి ఉత్పన్నమయ్యే లావాదేవీలను ఆమోదించగలదని దీని అర్థం. ఇది గ్యాస్-స్పాన్సర్ మరియు బ్యాచ్డ్ లావాదేవీల వంటి ఫీచర్లను అనుమతిస్తుంది. ఇది పని చేయడానికి, EVMకు రెండు కొత్త ఆప్‌కోడ్‌లను జోడించాలి: <code>AUTH</code> మరియు <code>AUTHCALL</code>. EIP-3074తో స్మార్ట్ కాంట్రాక్ట్ వాలెట్ యొక్క ప్రయోజనాలు <em>ఒప్పందం అవసరం లేకుండా</em> అందుబాటులోకి వచ్చాయి - బదులుగా, "ఇన్‌వోకర్" అని పిలువబడే నిర్దిష్ట రకం స్థితిలేని, విశ్వసనీయత లేని, అప్‌గ్రేడ్ చేయలేని ఒప్పందం లావాదేవీలను నిర్వహిస్తుంది.

EIP-3074 ప్రస్తుతం సక్రియంగా లేదని గమనించండి. సంఘం ప్రస్తుతం EIP-4337కు అనుకూలంగా ఉంది ఎందుకంటే దీనికి ప్రోటోకాల్‌లో మార్పులు అవసరం లేదు.

</ExpandableCard>

## ప్రస్తుత పురోగతి {#current-progress}

స్మార్ట్ కాంట్రాక్ట్ వాలెట్‌లు ఇప్పటికే అందుబాటులో ఉన్నాయి, అయితే వాటిని వీలైనంత వికేంద్రీకరించి అనుమతి లేకుండా చేయడానికి మరిన్ని అప్‌గ్రేడ్‌లు అవసరం. EIP-4337 అనేది Ethereum యొక్క ప్రోటోకాల్‌కు ఎటువంటి మార్పులు అవసరం లేని పరిపక్వ ప్రతిపాదన, కాబట్టి ఇది త్వరగా అమలు చేయబడే అవకాశం ఉంది. అయితే, Ethereum యొక్క ప్రోటోకాల్‌ను మార్చే అప్‌గ్రేడ్‌లు ప్రస్తుతం యాక్టివ్ డెవలప్‌మెంట్‌లో లేవు, కాబట్టి ఆ మార్పులు రవాణా చేయడానికి ఎక్కువ సమయం పట్టవచ్చు. EIP-4337 ద్వారా ఖాతా సంగ్రహణ తగినంతగా సాధించబడే అవకాశం ఉంది, దీనికి ఎటువంటి ప్రోటోకాల్ మార్పులు అవసరం లేదు.

## Further reading {#further-reading}

- [erc4337.io](https://www.erc4337.io/)
- [డెవ్‌కాన్ బొగోటా నుండి ఖాతా సంగ్రహణ ప్యానెల్ చర్చ](https://www.youtube.com/watch?app=desktop&v=WsZBymiyT-8)
- [డెవ్‌కాన్ బొగోటా నుండి ఎందుకు ఖాతా సంగ్రహణ అనేది dapps కోసం గేమ్ ఛేంజర్](https://www.youtube.com/watch?v=OwppworJGzs)
- [డెవ్‌కాన్ బొగోటా నుండి "ఖాతా సంగ్రహణ ELI5"](https://www.youtube.com/watch?v=QuYZWJj65AY)
- [విటాలిక్ యొక్క "రోడ్ టు అకౌంట్ అబ్‌స్ట్రాక్షన్" నోట్స్](https://notes.ethereum.org/@vbuterin/account_abstraction_roadmap#Transaction-inclusion-lists)
- [సోషల్ రికవరీ వాలెట్‌లపై విటాలిక్ బ్లాగ్ పోస్ట్](https://vitalik.eth.limo/general/2021/01/11/recovery.html)
- [EIP-2938 నోట్స్](https://hackmd.io/@SamWilsn/ryhxoGp4D#What-is-EIP-2938)
- [EIP-2938 డాక్యుమెంటేషన్](https://eips.ethereum.org/EIPS/eip-2938)
- [EIP-4337 నోట్స్](https://medium.com/infinitism/erc-4337-account-abstraction-without-ethereum-protocol-changes-d75c9d94dc4a)
- [EIP-4337 డాక్యుమెంటేషన్](https://eips.ethereum.org/EIPS/eip-4337)
- [EIP-2771 డాక్యుమెంటేషన్](https://eips.ethereum.org/EIPS/eip-2771)
- ["ఖాతా సంగ్రహణ యొక్క ప్రాథమిక అంశాలు" -- ఖాతా సంగ్రహణ పార్ట్ I అంటే ఏమిటి](https://www.alchemy.com/blog/account-abstraction)
