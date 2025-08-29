<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FAQ - Häufig gestellte Fragen</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            background-color: #f5f5f5;
        }
        
        .faq-container {
            background-color: white;
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        
        h1 {
            color: #333;
            text-align: center;
            margin-bottom: 30px;
            border-bottom: 3px solid #F78A27;
            padding-bottom: 10px;
        }
        
        .faq-item {
            margin-bottom: 20px;
            border: 1px solid #ddd;
            border-radius: 5px;
            overflow: hidden;
        }
        
        .faq-question {
            background-color: #f8f9fa;
            padding: 15px;
            cursor: pointer;
            font-weight: bold;
            color: #333;
            border-bottom: 1px solid #ddd;
            transition: background-color 0.3s ease;
        }
        
        .faq-question:hover {
            background-color: rgba(247, 138, 39, 0.1);
        }
        
        .faq-question::before {
            content: "+ ";
            color: #F78A27;
            font-weight: bold;
            margin-right: 10px;
        }
        
        .faq-answer {
            padding: 15px;
            background-color: white;
            color: #555;
            display: none;
        }
        
        .faq-answer.active {
            display: block;
        }
        
        .faq-question.active::before {
            content: "- ";
        }
        
        .faq-answer p {
            margin: 0;
        }
    </style>
</head>
<body>
    <div class="faq-container">
        <h1>Häufig gestellte Fragen (FAQ)</h1>
        
        <div class="faq-item">
            <div class="faq-question">
                Wie viele Personen nehmen an der Reise teil?
            </div>
            <div class="faq-answer">
                <p>Die Reise findet in kleinem Rahmen mit maximal 20-25 Teilnehmer:innen statt.</p>
            </div>
        </div>
        
        <div class="faq-item">
            <div class="faq-question">
                Was ist im Preis inkludiert?
            </div>
            <div class="faq-answer">
                <p>Programm & Kontaktkuratierung, Dolmetschung im Business‑Programm, Transfers laut Programm,  Business‑Dinner & Lunches, Medien‑Kurz‑Porträt. Flüge sind exklusive..</p>
            </div>
        </div>
        
        <div class="faq-item">
            <div class="faq-question">
                Wie läuft die Anmeldung ab?
            </div>
            <div class="faq-answer">
                <p>Wir empfehlen zunächst ein kostenfreies, unverbindliches 15-Minuten-Gespräch zu vereinbaren. Anschließend können Sie Ihre Anmeldung über unser Formular vornehmen.</p>
            </div>
        </div>
        
        <div class="faq-item">
            <div class="faq-question">
               Kann ich jemanden aus meinem Unternehmen mitnehmen?
            </div>
            <div class="faq-answer">
                <p>Selbstverständnlich können Sie zu zweit aus einem Unternehmen teilnehmen. Sprechen Sie uns hierzu direkt an.</p>
            </div>
        </div>

    <script>
        // FAQ Accordion Funktionalität
        document.addEventListener('DOMContentLoaded', function() {
            const questions = document.querySelectorAll('.faq-question');
            
            questions.forEach(question => {
                question.addEventListener('click', function() {
                    const answer = this.nextElementSibling;
                    
                    // Schließe alle anderen Antworten
                    questions.forEach(q => {
                        if (q !== this) {
                            q.classList.remove('active');
                            q.nextElementSibling.classList.remove('active');
                        }
                    });
                    
                    // Toggle aktuelle Antwort
                    this.classList.toggle('active');
                    answer.classList.toggle('active');
                });
            });
        });
    </script>
</body>
</html>
