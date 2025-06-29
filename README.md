## Description
Compilateur pour le langage TPC (sous-ensemble de C).  
Il effectue les étapes classiques de compilation :
- Analyse lexicale, syntaxique et sémantique
- Génération de code assembleur

# Utilisation
make
./bin/tpcc < fichier.tpc

#Options :

-t : affiche l’AST
-s : affiche la table des symboles

#Tests 
./run_tests.sh

# Sortie
Le compilateur génère un fichier _anonymous.asm contenant le code assembleur.


#Structure

```
.
├── src/         # Fichiers sources du compilateur
│   ├── codegen.c
│   ├── codegen.h
│   ├── lexer.l
│   ├── parser.y
│   ├── semantics.c
│   ├── semantics.h
│   ├── symbol_table.c
│   ├── symbol_table.h
│   ├── tree.c
│   └── tree.h
├── test/        # Jeux de tests
│   ├── good/
│   ├── sem-err/
│   ├── syn-err/
│   └── warn/
├── bin/         # Binaire compilé
├── obj/         # Objets intermédiaires
├── makefile
├── run_tests.sh
└── _anonymous.asm
```
