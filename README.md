# MYSQL_DB_SAMPLES
Database d'esempio di azienda venditrice di modellini di auto
con dati gia' inseriti.

Nomi di tabelle e colonne adattati in modo da essere in linea per docenze

VEDERE DIAGRAMMA ER PER RIFERIMENTO

PRODUCTLINES->CATEGORIA_PRODOTTO


  -RIMOSSI htmlDescription, image
  
  -textDescription->descrizione
  
EMPLOYEES->IMPIEGATO

  -RIMOSSI extension, jobTitle
  
  -employeeNumber->id
  
OFFICES->UFFICIO

  -RIMOSSI addressLine2, state, postalCode, territory
  
  -officeCode->codice
  
  -city->citta
  
  -phone->telefono
  
  -addressLine1->indirizzo
  

PRODUCTS->PRODOTTO

  -RIMOSSI productScale, productVendor, productDescription
  
  -productCode->codice
  
  -productLine->categoria
  
  -productDescription->descrizione
  
  -quantityInStock->quantita_stock
  
  -buyPrice->prezzo_di_acquisto
  
  -MSRP->prezzo_vendita_consigliato
  
  
CUSTOMERS->CLIENTE

  -RIMOSSI contactFirstName, contactLastName, phone, addressLine2, state, postalCode, creditLimit
  
  -customerNumber->id
  
  -customerName->nome
  
  -addressLine1->indirizzo
  
  -city->citta
  
  -state->stato
  
  -salesRepEmployeeNumber->id_impiegato (impiegato rappresentate assegnato al cliente)
  
  
ORDERDETAILS->DETTAGLI_ORDINE

  -RIMOSSI orderLineNumber
  
  -orderNumber->id_ordine
  
  -productCode->codice_prodotto
  
  -quantityOrdered->quantita
  
  
ORDERS->ORDINE

  -rimossi requiredDate, comments
  
  -orderNumber->id
  
  -orderDate->data_ordine
  
  -shippedDate->data_spedizione
  
  -customerNumber->id_cliente
  
  
PAYMENTS->PAGAMENTO

  -customerNumber->id_cliente
  
  -checkNumber->codice_assegno
  
  -paymentDate->data
  
  -amount->importo
