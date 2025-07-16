---
lab:
  title: "Lab\_5: Schaltflächen-Flow"
  module: 'Module 4: Build flows to manage user information'
---

# Übungs-Lab 5 – Schaltflächen-Flow

In diesem Lab erstellen Sie einen Schaltflächen-Flow.

## Lernziele

- So erstellen Sie einen Power Automate-Sofortschaltflächen-Flow

## Weiterführende Schritte des Lab

- Einen Flow für eine Schaltfläche erstellen
- Verwenden von Triggertokens
- Benutzereingabe hinzufügen
- Testen des Flows
  
## Voraussetzungen

- Sie müssen **Lab 2: Datenmodell** abgeschlossen haben

## Ausführliche Schritte

## Übung 1 – Schaltflächen-Flow erstellen

### Aufgabe 1.1 – Erstellen des Triggers

1. Navigieren Sie zum Power Automate-Portal `https://make.powerautomate.com`.

1. Vergewissern Sie sich, dass Sie sich in der Umgebung **Dev One** befinden.

1. Wählen Sie im linken Menü die Registerkarte **+ Erstellen** aus.

1. Wählen Sie **+ Sofortiger Cloud-Flow** aus.

1. Geben Sie `Create opportunity` als **Flowname** ein.

1. Wählen Sie **Manuell einen Flow auslösen**.

1. Klicken Sie auf **Erstellen**.


### Aufgabe 1.2 – Hinzufügen von Benutzereingaben

1. Wählen Sie den Schritt **Manuell einen Flow triggern** aus.

1. Wählen Sie die Schrittbezeichnung **Manuell einen Flow auslösen** aus und geben Sie `Button triggered` ein.

1. Wählen Sie **Eingabe hinzufügen** aus.

1. Wählen Sie **Text** aus.

1. Geben Sie `Customer Name` in **Eingabe** ein.

1. Geben Sie `Please enter the customer name` in **Bitte geben Sie Ihre Eingabe ein**.

1. Wählen Sie **Eingabe hinzufügen** aus.

1. Wählen Sie **Text** aus.

1. Geben Sie `Comments` in **Eingabe** ein.

1. Geben Sie `Any comments` in **Bitte geben Sie Ihre Eingabe ein**.

1. Wählen Sie **Eingabe hinzufügen** aus.

1. Wählen Sie **Nummer** aus.

1. Geben Sie `Potential Sale` in **Nummer** ein.

    ![Screenshot der Benutzereingabe.](../media/user-input.png)


### Aufgabe 1.3 – Aktion zum Erstellen von Verkaufschancen hinzufügen

1. Wählen Sie unter dem Trigger-Schritt das Symbol **+** aus, und wählen Sie **Aktion hinzufügen** aus.

1. Geben Sie `add row` in das Suchfeld ein.

1. Wählen Sie **Eine neue Zeile hinzufügen** unter **Microsoft Dataverse**.

1. Wählen Sie **Anmelden** aus

1. Verwenden Sie Ihre Mandantenanmeldeinformationen.

1. Wählen Sie den Schritt **Neue Zeile hinzufügen** und geben Sie `New opportunity` ein.

1. Wählen Sie **Möglichkeiten** für **Tabellenname**.

1. Geben Sie `/` in das Feld **Kunde** ein und wählen Sie **Dynamischen Inhalt einfügen** aus und klicken Sie auf **Mehr anzeigen**.

1. Wählen Sie **Kundenname** aus.

1. Wählen Sie das Feld **Besitzername** und geben Sie `MOD Administrator` ein.

1. Wählen Sie **Alle anzeigen** aus.

1. Wählen Sie das Feld **Betreff der Möglichkeit** und geben Sie `New opportunity` ein.

1. Geben Sie `/` in das Feld **Betrag** ein und wählen Sie **Dynamischen Inhalt einfügen**.

1. Wählen Sie **Potenzielles Sonderangebot** aus.

1. Wählen Sie das Feld **Notizen**, das Symbol „Dynamischer Inhalt“ und dann **Weitere anzeigen** aus.

1. Wählen Sie **Kommentare** aus.

1. Geben Sie `/` in das Feld **Geschätztes Abschlussdatum** ein und wählen Sie **Ausdruck einfügen**.

1. Geben Sie den Ausdruck `utcNow()` ein und wählen Sie **Hinzufügen** aus.

    ![Screenshot der neuen Opportunity-Aktion.](../media/new-opportunity-action.png)

1. Wählen Sie **Speichern**.


## Übung 2 – Schaltflächen-Flow testen

### Aufgabe 2.1 – Schaltflächen-Flow ausführen

1. Klicken Sie auf **Testen**.

1. Wählen Sie **Manuell** aus.

1. Klicken Sie auf **Test**.

    ![Screenshot vom Testen des Schaltflächen-Flows.](../media/user-input-test.png)

1. Geben Sie die folgenden Details ein:

   1. Kundenname=`Button test`
   1. Kommentare=`This is a test`
   1. Potenzielles Sonderangebot=`9999`

1. Wählen Sie **Flow ausführen** aus.

1. Wählen Sie **Fertig** aus.

1. Wählen Sie die **<-**-Schaltfläche „Zurück“ oben links in der Befehlsleiste aus.


### Aufgabe 2.2 – Überprüfen des erstellten Opportunity-Datensatzes

1. Navigieren Sie zum Power Apps Maker-Portal `https://make.powerapps.com`.

1. Stellen Sie sicher, dass Sie sich in der Umgebung **Dev One** befinden.

1. Wählen Sie im linken Navigationsbereich **Tabellen** aus.

1. Wählen Sie **Verkaufschance** aus.

