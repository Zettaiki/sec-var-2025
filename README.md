# sec-var-2025
*Segmentazione di edifici da immagini satellitari e classificazione del contesto urbano.*

Il progetto consiste nello sviluppo di un modello di deep learning in grado di eseguire la segmentazione semantica delle immagini satellitari, identificando gli edifici e classificandoli in diverse categorie in base a caratteristiche specifiche.

Il dataset utilizzato per questo progetto è il dataset [Inria Aerial Image Labeling Dataset](https://project.inria.fr/aerialimagelabeling/).

## Requisiti

### Hardware

Questo progetto richiede una significativa potenza di calcolo. Si consiglia di utilizzare una GPU per addestrare il modello in modo efficiente o di considerare l'utilizzo di servizi cloud con GPU dedicate.

- 50 GB di spazio libero su disco

### Software

- Python 3.10 (with Jupyter Notebook)
- Dataset [Inria Aerial Image Labeling Dataset](https://project.inria.fr/aerialimagelabeling/)

> **Nota:** Assicurati di avere accesso al dataset e di averlo scaricato nella directory corretta prima di eseguire il progetto.

## Struttura del Progetto

Il progetto è organizzato nella seguente struttura di directory:

```
src
`-- python
    |-- 1_model_training.ipynb
    |-- 2_classification.ipynb
    `-- model
        `-- UnetWSatellite.keras
```

## Configurazione ed esecuzione

Dopo aver verificato i requisiti, per configurare il progetto bisogna eseguire i seguenti passaggi:

1. **Clonare il repository**:

```bash
git clone https://github.com/Zettaiki/sec-var-2025.git
cd sec-var-2025
```

2. **Installare le dipendenze Python**: Assicurati di avere Python 3.10 e Jupyter Notebook installati.

```bash
pip install -r requirements.txt
```

> Puoi anche utilizzare un ambiente virtuale per isolare le dipendenze del progetto, ad esempio utilizzando [Miniconda](https://www.anaconda.com/download/success) o venv.

3. **Eseguire i notebook**: I notebook Jupyter possono essere eseguiti direttamente da Jupyter Lab o Jupyter Notebook. Assicurati di avere il kernel Python corretto selezionato.

I notebook presenti in questo progetto rappresentano le due fasi principali:

- `1_model_training.ipynb`: Questo notebook si occupa dell'addestramento del modello di segmentazione semantica utilizzando il dataset fornito.
- `2_classification.ipynb`: Questo notebook si occupa della classificazione degli edifici segmentati in diverse categorie.

Il primo notebook si concentra sull'addestramento del modello utilizzando il dataset di immagini aeree, e produce come risultato un modello addestrato salvato nella directory `src/python/model/`.

> Nella repository è presente un modello pre-addestrato che può essere utilizzato per la classificazione degli edifici.

Il secondo notebook si occupa della classificazione degli edifici segmentati in diverse categorie utilizzando il modello addestrato. Questo notebook utilizza il modello salvato nella directory `src/python/model/` per effettuare le previsioni sulle immagini aeree e classificare gli edifici in base alle loro caratteristiche.

## Licenza

Questo progetto è concesso in licenza sotto i termini della licenza MIT – vedi il file [LICENSE](LICENSE) per maggiori dettagli.

La licenza MIT è una licenza semplice e permissiva che permette agli utenti di:

- Utilizzare il software per qualsiasi scopo
- Modificare il software per adattarlo alle proprie esigenze
- Distribuire copie del software
- Includere il software in progetti proprietari

Il software è fornito "così com'è", senza alcuna garanzia.

Per maggiori informazioni sulla licenza MIT, visita:
https://opensource.org/licenses/MIT