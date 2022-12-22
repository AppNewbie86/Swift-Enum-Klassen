# Swift-Enum-Klassen
Mein Nachschlagewerk in Sachen Enum Classes


import UIKit

//------------------------------Interaktive Aufgabe 10 Min Zeit---------------------------------------


// Enum Klassen und ihre Verwendung

// wird auch als Aufzählung definiert (gemeinsamer Typ einer Gruppe mit gleichem Werten)
// sind wie Structuren auch Wertetypen
// Dienen der Gruppierung von Werten haben jedoch keine eigenen Eigenschaften
// Werte werden hier als cases bezeichnet


enum Wochentag : CaseIterable{
    case monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday
}

var day = Wochentag.allCases.randomElement()!

switch day {
case .monday:print("heute ist Montag")
case .Tuesday:print("heute ist dienstag")
case .Wednesday:print("heute ist mittwoch")
case .Thursday:print("heute ist donnerstag")
case .Friday:print("heute ist freitag")
case .Saturday:print("heute ist samstag")
case .Sunday:print("heute ist sonntag")
    
}


//------------------------------------------------------1. Aufgabe -------------------------------------

// Compass

// Werteklasse die von CaseIterable erbt
enum Compass : CaseIterable {
    // Case beschreibt den Inhalt
    case Norden, Osten, Süden, Westen
}


// Variable zum Speichern des RandomElements wo dann darüber abgerufen werden kann
var compass = Compass.allCases.randomElement()!
// Verzweigung auf die Antworten
switch compass {
case.Norden: print("Im Norden, ist sie nie zu sehen")
case .Osten: print("Im Osten, geht die Sonne auf")
case .Süden: print("Im Süden, nimmt sie ihren Lauf")
case .Westen: print("Im Westen, will sie untergeh'n")
}




//------------------------------------------------------2. Aufgabe -------------------------------------

// Weather

// Werteklasse die von CaseIterable erbt
enum Weather : CaseIterable {
    // Case beschreibt den Inhalt
    case Sonnig, Regnerisch, Stuermig, Windig
}
// Variable zum Speichern des RandomElements wo dann darüber abgerufen werden kann
var weather = Weather.allCases.randomElement()!

// hier vergleicht der den Getroffenen Fall mit der Wettersituation und druckt den dementsprechenden Text raus
switch weather {
case.Sonnig: print("Heute brauch man keinen Regenschirm")
case .Regnerisch: print("Das regenrisiko ist sehr hoch, nehmen sie zu ihrer Sicherheit einen Schirm mit")
case .Windig: print("Heute regnet es nicht aber ziehen sie sich warme Kleidung an ")
case .Stuermig: print("Es ist drsaussen sehr stuermig")
    
}


//------------------------------------------------------3. Aufgabe -------------------------------------

// Orakel


// Werteklasse die von CaseIterable erbt

enum Orakel: CaseIterable{
    // Inhalt des Cases
    case positiv, neutral, negativ
    static func random() -> Orakel{
        return allCases.randomElement()!
    }
}

// Array 1
let positivArray = ["Sauber Kerle","Ja hop weiter so"]

// Array 2
let neutralArray = ["sollte eventuell passen","Vielleicht"]

// Array 3
let negativArray = ["No No ","No Chance"]


// Variable gesetzt wo die Situation random abspeichert
var situation = Orakel.random()
// Verzweigung auf die Antworten
switch situation {
case.positiv: print(positivArray.randomElement()!)
case.neutral: print(neutralArray.randomElement()!)
case.negativ: print(negativArray.randomElement()!)
}

