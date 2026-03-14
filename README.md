# Mit főzzek ma. AI által generált recept kiíratása UI-ra
Garantáltan asszonyfaktor növelő elem a Home Assistantba :)

Nálunk a HA-ba már egy ideje be van integrálva az OpenAI. Próbálom sulykolni a családot, hogy használják, kérdezzenek tőle. Azt is mondtam a feleségemnek, hogy ha nincs ötlete, hogy mit főzzön kérdezze meg az AI-t, hogy van e valami jó ötlete. Ez idáig ok. Az AI elmondja a receptet, el is ismételheti, de szar mindig kérdezgetni, ha elfelejtesz valamit. Azt akartam megoldani, hogy a receptet a dashboard egy meghatározott helyére írja ki. Így főzés közben bármikor visszanézhető az utoljára kért recept. 

Ehhez egy eseményvezérelt (trigger-based) Template Senzort fogunk használni. Ennek az a hatalmas előnye, hogy bármilyen hosszú szöveget be lehet tölteni.

### És akkor íme a hozzávalók: ### 

### 1. Az angol Prompt az OpenAI-hoz ###

Nálunk kétfajta OpenAI Conversation van. Egy angol és egy magyar. Itt most a magyar OpenAI Conversation beállításait irom le. 
Másold be ezt a szöveget az OpenAI Conversation integráció utasítás (prompt) mezőjébe:

### When the user asks for a recipe, generate the complete recipe including ingredients and step-by-step instructions. You MUST use the available tool/script named 'Show recipe on ui' to pass the full text of this recipe to the dashboard. ###

Ha akarod még kiegészítheted ezekkel is: 
### Important: Do NOT read the full recipe out loud. Verbally, you must reply ONLY with this short confirmation in Hungarian: "A kért receptet megjelenítettem a telefonodon." ###
