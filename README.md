# Multithreaded Binomial Calculator

Progetto Java per il calcolo del coefficiente binomiale tramite programmazione concorrente.

##  Descrizione
Il programma calcola la combinazione $C(n, k)$ dividendo il carico di lavoro su tre Thread distinti per massimizzare l'efficienza dei calcoli fattoriali.

### Funzionamento dei Thread:
* **Thread N!**: Calcola il fattoriale di $n$.
* **Thread K!**: Calcola il fattoriale di $k$.
* **Thread (N-K)!**: Calcola il fattoriale della differenza.

Il programma utilizza il metodo `.join()` per attendere il completamento di tutti i calcoli prima di applicare la formula finale:
$$C(n, k) = \frac{n!}{k!(n-k)!}$$



##  Tecnologie e Concetti
* **Java Core**: Utilizzo della classe `Thread`.
* **Sincronizzazione**: Gestione del ciclo di vita dei thread (start/join).
* **Exception Handling**: Gestione di input non validi e numeri negativi tramite eccezione personalizzata `NumeroNegativo`.
