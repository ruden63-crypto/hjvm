<!DOCTYPE html>
<html lang="kk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bauyrzhan Beissenbay - Portfolio</title>
    <!-- Cloudflare cdnjs арқылы html2pdf кітапханасын қосу -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/html2pdf.js/0.10.1/html2pdf.bundle.min.js"></script>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f4f6f9;
            margin: 0;
            padding: 20px;
        }
        .controls {
            text-align: center;
            margin-bottom: 20px;
        }
        .btn-download {
            background-color: #0056b3;
            color: white;
            border: none;
            padding: 12px 24px;
            font-size: 16px;
            font-weight: bold;
            border-radius: 6px;
            cursor: pointer;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            transition: background 0.3s;
        }
        .btn-download:hover {
            background-color: #003d82;
        }
        /* PDF парағының стандарты A4 */
        .pdf-page {
            width: 210mm;
            min-height: 297mm;
            padding: 20mm;
            margin: 0 auto;
            background: white;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
            box-sizing: border-box;
            color: #333;
        }
        h1 {
            color: #1a365d;
            margin-bottom: 5px;
            font-size: 24pt;
            text-transform: uppercase;
        }
        .subtitle {
            color: #4a5568;
            font-size: 11pt;
            margin-bottom: 20px;
            border-bottom: 2px solid #e2e8f0;
            padding-bottom: 10px;
        }
        .section-title {
            color: #2b6cb0;
            font-size: 13pt;
            border-bottom: 1.5px solid #2b6cb0;
            margin-top: 18px;
            margin-bottom: 8px;
            padding-bottom: 3px;
            text-transform: uppercase;
        }
        ul {
            margin: 5px 0;
            padding-left: 20px;
        }
        li {
            margin-bottom: 5px;
            font-size: 10pt;
            line-height: 1.4;
        }
        .item-header {
            font-weight: bold;
            color: #2d3748;
        }
        .text-sm {
            font-size: 9.5pt;
            color: #4a5568;
        }
    </style>
</head>
<body>

    <div class="controls">
        <button class="btn-download" onclick="downloadPDF()">PDF болып жүктеу</button>
    </div>

    <!-- PDF контейнері -->
    <div class="pdf-page" id="portfolio-content">
        <h1>BAUYRZHAN BEISSENBAY</h1>
        <div class="subtitle">
            Almaty, Kazakhstan | Target: Sophia University (International Law)
        </div>

        <div class="section-title">Education</div>
        <ul>
            <li><span class="item-header">FIZTEX High School</span> (Almaty, Kazakhstan) — Expected Graduation: 2028</li>
            <li class="text-sm">Track: Social Sciences, Legal Studies & International Relations</li>
        </ul>

        <div class="section-title">Academic Honors & Olympiads (5 Awards)</div>
        <ul>
            <li><span class="item-header">1st Place / Gold Medalist</span> — National/Regional Law & Humanities Olympiad</li>
            <li><span class="item-header">2nd Place / Silver Medalist</span> — City Social Sciences Competition</li>
            <li><span class="item-header">3rd Place / Bronze Medalist</span> — History & Legal Studies Olympiad</li>
            <li><span class="item-header">Finalist & Laureate</span> — Republican Legal Rights Challenge</li>
            <li><span class="item-header">Diploma Winner</span> — Regional Jurisprudence & Debate Tournament</li>
        </ul>

        <div class="section-title">Key Projects (3 Projects)</div>
        <ul>
            <li>
                <span class="item-header">International Law & Human Rights Research</span><br>
                <span class="text-sm">Conducted analytical studies on global human rights frameworks and international treaty enforcement mechanisms.</span>
            </li>
            <li>
                <span class="item-header">Youth Legal Literacy Initiative</span><br>
                <span class="text-sm">Organized interactive workshops and legal awareness campaigns for high school students.</span>
            </li>
            <li>
                <span class="item-header">Chess & Diplomatic Strategy Club</span><br>
                <span class="text-sm">Founded a school initiative connecting competitive chess strategic principles with international dispute resolution models.</span>
            </li>
        </ul>

        <div class="section-title">Certifications (4 Credentials)</div>
        <ul>
            <li><span class="item-header">IELTS / TOEFL Certificate</span> — Academic English Proficiency</li>
            <li><span class="item-header">International Law Online Course</span> — Certified Credential (Coursera/edX)</li>
            <li><span class="item-header">Model United Nations (MUN)</span> — Best Delegate / Conference Certificate</li>
            <li><span class="item-header">Leadership & Public Speaking</span> — Advanced Training Certification</li>
        </ul>

        <div class="section-title">Skills & Languages</div>
        <ul>
            <li><span class="item-header">Languages:</span> Kazakh (Native), English (Academic), Russian (Fluent)</li>
            <li><span class="item-header">Strategic Thinking:</span> Competitive Chess Player (Logic, Strategic Planning & Crisis Management)</li>
            <li><span class="item-header">Core Competencies:</span> Legal Analysis, Public Speaking, Negotiation, Policy Research</li>
        </ul>
    </div>

    <script>
        function downloadPDF() {
            const element = document.getElementById('portfolio-content');
            const opt = {
                margin:       0,
                filename:     'Bauyrzhan_Beissenbay_Portfolio.pdf',
                image:        { type: 'jpeg', quality: 0.98 },
                html2canvas:  { scale: 2 },
                jsPDF:        { unit: 'mm', format: 'a4', orientation: 'portrait' }
            };

            // HTML-ді PDF-ке айналдыру және жүктеу
            html2pdf().set(opt).from(element).save();
        }
    </script>
</body>
</html>
