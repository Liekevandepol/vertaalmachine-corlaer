# vertaalmachine-corlaer
vertaalmachine
#!/usr/bin/env python3
"""
Nederlandse naar Spaanse Offline Vertaalmachine
Dit programma vertaalt Nederlandse woorden naar het Spaans zonder internetverbinding.
"""

class NederlandsSpaans_Vertaalmachine:
    """Een eenvoudige offline vertaalmachine voor Nederlands naar Spaans"""
    
    def __init__(self):
        """Initialiseer de woordenboeken voor vertaling"""
        # Basiswoordenboek: Nederlands -> Spaans
        self.woordenboek = {
            # Dagelijkse woorden
            'hallo': 'hola',
            'dag': 'adiós',
            'goedemorgen': 'buenos días',
            'goedemiddag': 'buenas tardes',
            'goedenavond': 'buenas noches',
            'dank je wel': 'gracias',
            'dank u': 'gracias',
            'alstublieft': 'por favor',
            'ja': 'sí',
            'nee': 'no',
            'excuses': 'perdón',
            'sorry': 'lo siento',
            
            # Voedsel en drinken
            'water': 'agua',
            'koffie': 'café',
            'thee': 'té',
            'brood': 'pan',
            'kaas': 'queso',
            'melk': 'leche',
            'vlees': 'carne',
            'vis': 'pescado',
            'groente': 'verdura',
            'fruit': 'fruta',
            'appel': 'manzana',
            'banaan': 'plátano',
            'sinaasappel': 'naranja',
            'aardappel': 'papa',
            'tomaat': 'tomate',
            'ijs': 'helado',
            'chocolade': 'chocolate',
            
            # Familie
            'vader': 'padre',
            'moeder': 'madre',
            'broer': 'hermano',
            'zus': 'hermana',
            'opa': 'abuelo',
            'oma': 'abuela',
            'zoon': 'hijo',
            'dochter': 'hija',
            'man': 'marido',
            'vrouw': 'esposa',
            'oom': 'tío',
            'tante': 'tía',
            'neef': 'primo',
            'nicht': 'prima',
            
            # Lichaamsdelen
            'hoofd': 'cabeza',
            'oog': 'ojo',
            'oor': 'oído',
            'neus': 'nariz',
            'mond': 'boca',
            'tand': 'diente',
            'tong': 'lengua',
            'hand': 'mano',
            'vinger': 'dedo',
            'voet': 'pie',
            'been': 'pierna',
            'arm': 'brazo',
            'hart': 'corazón',
            'longen': 'pulmones',
            'maag': 'estómago',
            
            # Kleren
            'shirt': 'camisa',
            'broek': 'pantalón',
            'rok': 'falda',
            'jurk': 'vestido',
            'jas': 'chaqueta',
            'schoenen': 'zapatos',
            'sokken': 'calcetines',
            'hoed': 'sombrero',
            'muts': 'gorro',
            'handschoenen': 'guantes',
            'sjaal': 'bufanda',
            'pet': 'gorra',
            
            # Getallen
            'nul': 'cero',
            'een': 'uno',
            'twee': 'dos',
            'drie': 'tres',
            'vier': 'cuatro',
            'vijf': 'cinco',
            'zes': 'seis',
            'zeven': 'siete',
            'acht': 'ocho',
            'negen': 'nueve',
            'tien': 'diez',
            'elf': 'once',
            'twaalf': 'doce',
            'dertien': 'trece',
            'veertien': 'catorce',
            'vijftien': 'quince',
            'twintig': 'veinte',
            'dertig': 'treinta',
            'veertig': 'cuarenta',
            'vijftig': 'cincuenta',
            'zestig': 'sesenta',
            'zeventig': 'setenta',
            'tachtig': 'ochenta',
            'negentig': 'noventa',
            'honderd': 'cien',
            'duizend': 'mil',
            
            # Kleuren
            'rood': 'rojo',
            'blauw': 'azul',
            'groen': 'verde',
            'geel': 'amarillo',
            'oranje': 'naranja',
            'paars': 'púrpura',
            'zwart': 'negro',
            'wit': 'blanco',
            'grijs': 'gris',
            'bruin': 'marrón',
            'roze': 'rosa',
            
            # Weer
            'zon': 'sol',
            'maan': 'luna',
            'ster': 'estrella',
            'wolk': 'nube',
            'regen': 'lluvia',
            'sneeuw': 'nieve',
            'wind': 'viento',
            'donder': 'trueno',
            'bliksem': 'rayo',
            'hagel': 'granizo',
            'mist': 'niebla',
            
            # Dieren
            'hond': 'perro',
            'kat': 'gato',
            'vogel': 'pájaro',
            'vis': 'pez',
            'konijn': 'conejo',
            'muis': 'ratón',
            'rat': 'rata',
            'paard': 'caballo',
            'koe': 'vaca',
            'kip': 'gallina',
            'eend': 'pato',
            'gans': 'ganso',
            'slang': 'serpiente',
            'schildpad': 'tortuga',
            'kikker': 'rana',
            'vlinder': 'mariposa',
            'bij': 'abeja',
            'spin': 'araña',
            'leeuw': 'león',
            'tijger': 'tigre',
            'beer': 'oso',
            'aap': 'mono',
            'olifant': 'elefante',
            
            # Acties/werkwoorden
            'lopen': 'caminar',
            'rennen': 'correr',
            'springen': 'saltar',
            'vliegen': 'volar',
            'zwemmen': 'nadar',
            'schrijven': 'escribir',
            'lezen': 'leer',
            'zingen': 'cantar',
            'dansen': 'bailar',
            'spelen': 'jugar',
            'eten': 'comer',
            'drinken': 'beber',
            'slapen': 'dormir',
            'waken': 'despertarse',
            'werken': 'trabajar',
            'studeren': 'estudiar',
            'luisteren': 'escuchar',
            'kijken': 'mirar',
            'zien': 'ver',
            'horen': 'oír',
            'spreken': 'hablar',
            'praten': 'charlar',
            'denken': 'pensar',
            'voelen': 'sentir',
            'ruiken': 'oler',
            'proeven': 'probar',
            'maken': 'hacer',
            'bouwen': 'construir',
            'breken': 'romper',
            'repareren': 'reparar',
            'wassen': 'lavar',
            'koken': 'cocinar',
            'bakken': 'hornear',
            'rijden': 'conducir',
            'varen': 'navegar',
        }
        
    def vertaal_woord(self, nederlands_woord):
        """
        Vertaal een Nederlands woord naar het Spaans
        
        Args:
            nederlands_woord (str): Het woord dat vertaald moet worden
            
        Returns:
            str: Het vertaalde woord of bericht dat het woord niet gevonden is
        """
        woord_schoon = nederlands_woord.strip().lower()
        
        if woord_schoon in self.woordenboek:
            return self.woordenboek[woord_schoon]
        else:
            return f"Sorry, '{nederlands_woord}' is niet in het woordenboek."
    
    def vertaal_zin(self, nederlandse_zin):
        """
        Vertaal een hele Nederlandse zin naar het Spaans
        
        Args:
            nederlandse_zin (str): De zin die vertaald moet worden
            
        Returns:
            str: De vertaalde zin
        """
        woorden = nederlandse_zin.strip().split()
        vertaalde_woorden = []
        
        for woord in woorden:
            # Verwijder interpunctie
            interpunctie = ""
            schoon_woord = woord
            
            if woord and woord[-1] in ".,!?;:":
                interpunctie = woord[-1]
                schoon_woord = woord[:-1]
            
            # Vertaal het woord
            if schoon_woord.lower() in self.woordenboek:
                vertaald = self.woordenboek[schoon_woord.lower()]
                # Behoud de hoofdletters uit het origineel
                if schoon_woord and schoon_woord[0].isupper():
                    vertaald = vertaald.capitalize()
                vertaalde_woorden.append(vertaald + interpunctie)
            else:
                vertaalde_woorden.append(woord)
        
        return " ".join(vertaalde_woorden)
    
    def voeg_woord_toe(self, nederlands_woord, spaans_woord):
        """
        Voeg een nieuw woord toe aan het woordenboek
        
        Args:
            nederlands_woord (str): Het Nederlandse woord
            spaans_woord (str): Het Spaanse woord
        """
        self.woordenboek[nederlands_woord.lower()] = spaans_woord.lower()
        print(f"Woord toegevoegd: '{nederlands_woord}' -> '{spaans_woord}'")
    
    def toon_menu(self):
        """Toon het interactieve menu"""
        print("\n" + "="*50)
        print("NEDERLANDSE-SPAANSE VERTAALMACHINE")
        print("="*50)
        print("1. Vertaal een woord")
        print("2. Vertaal een zin")
        print("3. Voeg een woord toe aan woordenboek")
        print("4. Toon aantal woorden in woordenboek")
        print("5. Afsluiten")
        print("="*50)


def main():
    """Hoofdfunctie voor het programma"""
    vertaalmachine = NederlandsSpaans_Vertaalmachine()
    
    while True:
        vertaalmachine.toon_menu()
        keuze = input("\nMaak een keuze (1-5): ").strip()
        
        if keuze == "1":
            woord = input("Voer een Nederlands woord in: ")
            result = vertaalmachine.vertaal_woord(woord)
            print(f"\nVertaling: {result}\n")
        
        elif keuze == "2":
            zin = input("Voer een Nederlandse zin in: ")
            result = vertaalmachine.vertaal_zin(zin)
            print(f"\nVertaling: {result}\n")
        
        elif keuze == "3":
            nederlands = input("Voer het Nederlandse woord in: ")
            spaans = input("Voer het Spaanse woord in: ")
            vertaalmachine.voeg_woord_toe(nederlands, spaans)
        
        elif keuze == "4":
            aantal = len(vertaalmachine.woordenboek)
            print(f"\nHet woordenboek bevat {aantal} woorden.\n")
        
        elif keuze == "5":
            print("\nDank je wel voor het gebruik van de vertaalmachine!")
            print("Tot ziens!")
            break
        
        else:
            print("\nOngeldige keuze. Probeer opnieuw.\n")


if __name__ == "__main__":
    main()
