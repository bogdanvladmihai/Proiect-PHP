# Proiect-PHP

# Structura Bazei de Date a Departamentului Băncii

## Tabele

### Tabelul "Clienti"
- `id_client` (cheie primară)
- `nume`
- `prenume`
- `data nasterii`
- `tara`

### Tabelul "Conturi"
- `id_cont` (cheie primară)
- `id_client` (cheie străină către "Clienti")
- `data_deschidere`
- `data_expirare`
- `moneda`

### Tabelul "Tranzactii"
- `id_tranzactie` (cheie primară)
- `id_cont_beneficiar` (cheie străină către "Conturi")
- `id_cont_tranzactionar` (cheie străină către "Conturi")
- `suma`
- 'data'
- 'stare'

### Tabelul "Firma"
- `id_firma` (cheie primară)
- `nume`
- `data_infiintare`
- `tara`

### Tabelul "Angajat"
- `id_angajat` (cheie primară)
- `nume`
- `prenume`
- `data_angajare`
- `salariu`

# Descriere a Aplicației Bancare

Aplicația este un portal al unei bănci. Se pot crea conturi (de client sau de angajat), fiecare dintre aceste roluri având anumite privilegii.

## Funcționalități pentru Clienți:
- **Crearea Conturilor:** Clienții pot crea și gestiona conturi bancare personale.
- **Vizualizarea Tranzacțiilor:** Utilizatorii pot verifica istoricul tranzacțiilor și să vadă detaliile tranzacțiilor anterioare.
- **Realizarea de Tranzacții:** Clienții pot efectua depuneri, retrageri și transferuri.
- **Cererea de Deschidere Conturi:** Utilizatorii pot depune cereri pentru a deschide noi conturi bancare.

## Funcționalități pentru Angajați:
- **Aprobarea Conturilor:** Angajații au dreptul de a aproba sau respinge cererile de deschidere a conturilor de către clienți.
- **Vizualizarea și Interogarea Tranzacțiilor:** Angajații pot accesa și interoga întregul istoric al tranzacțiilor bancare.
- **Gestionarea Tranzacțiilor:** Angajații pot efectua tranzacții specifice.

## Administrație:
- **Aprobarea Conturilor Angajaților:** Un administrator poate aproba sau respinge cererile de creare a conturilor pentru angajați, asigurând controlul și securitatea accesului.

