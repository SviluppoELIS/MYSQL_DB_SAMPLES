# MYSQL_DB_SAMPLES
Database d'esempio di azienda venditrice di modellini di auto
con dati gia' inseriti.

Nomi di tabelle e colonne adattati in modo da essere in linea per docenze

productlines->categoria_prodotto
  -rimossi htmlDescription, image
  -textDescription->descrizione
  
employees->impiegato
  -rimossi extension, jobTitle
  -employeeNumber->id
  
offices->ufficio
  -rimossi addressLine2, state, postalCode, territory
  -officeCode->codice
  -city->citta
  -phone->telefono
  -addressLine1->indirizzo

products->prodotto
  -rimossi productScale, productVendor, productDescription
  -productCode->codice
  -productLine->categoria
  -productDescription->descrizione
  -quantityInStock->quantita_stock
  -buyPrice->prezzo_di_acquisto
  -MSRP->prezzo_vendita_consigliato
  
customers->cliente
  -rimossi contactFirstName, contactLastName, phone, addressLine2, state, postalCode, creditLimit
  -customerNumber->id
  -customerName->nome
  -addressLine1->indirizzo
  -city->citta
  -state->stato
  -salesRepEmployeeNumber->id_impiegato (impiegato rappresentate assegnato al cliente)
  
orderdetaile->dettagli_ordine
  -rimossi orderLineNumber
  -orderNumber->id_ordine
  -productCode->codice_prodotto
  -quantityOrdered->quantita
  
orders->ordine
  -rimossi requiredDate, comments
  -orderNumber->id
  -orderDate->data_ordine
  -shippedDate->data_spedizione
  -customerNumber->id_cliente
  
payments->pagamento
  -customerNumber->id_cliente
  -checkNumber->codice_assegno
  -paymentDate->data
  -amount->importo
