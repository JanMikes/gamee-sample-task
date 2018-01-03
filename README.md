# Gamee sample task

Zadáním je vytvořit API endpoint pro ukládání score ze hry a endpoint pro zobrazení prvních 10 hráčů pro konkrétní hru určenou v parametrech requestu.

Client (např JavaScript) zasílá po dohrání hry xhr request na server ve schématu jsonrpc (http://www.jsonrpc.org/specification). Payload requestu nese: ID hry (int), ID usera (int) a nahrané score (int).
PHP aplikace přijme request, uloží data do žebříčku a vrátí success odpověď. Je jedno, zda aplikace poběží přes php fpm, php server nebo cokoliv jiného.

### Technologické požadavky:
- Použití nette/di
- Ukládání žebříčku do nějaké vhodné datové struktury Redisu (screw data persistency)

### Validace vstupních dat:
- Určitě by bylo vhodné zvalidovat vstup
- Na nevalidní vstup potom smysluplně odpovídat (opět podle jsonrpc specky)

### Bonusové body:
- Krásné by bylo, kdybych si vyklonoval git repo, napsal `docker-compose up` a aplikace byla nastartovaná na předem daném portu
- Ještě krásnější by bylo, kdyby měli lidé pro stejné skóre stejný rank/pozici
