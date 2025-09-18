# make_readme.py
# Erstellt eine README.md mit den vom Nutzer gewünschten Texten
# Kodierung: UTF-8

import pathlib

README_PATH = pathlib.Path("README.md")

# Der exakte Text, so wie vom Benutzer gewünscht
content = """WHEN YOU WONT TO FIVEM CHEAT HIT ME PER DM
and if you interestet if making own discord bot then text kme
made by ecu
"""

def create_readme(path: pathlib.Path, text: str) -> None:
    """
    Schreibt die README.md (überschreibt, falls sie schon existiert).
    """
    path.write_text(text, encoding="utf-8")
    print(f"README.md wurde erstellt/überschrieben: {path.resolve()}")

def print_text(text: str) -> None:
    """
    Gibt den Text auf der Konsole aus.
    """
    print("---- Inhalt ----")
    print(text)
    print("---- Ende ----")

def main():
    create_readme(README_PATH, content)
    print_text(content)

if __name__ == "__main__":
    main()
