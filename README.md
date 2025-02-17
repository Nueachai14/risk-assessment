# risk-assessment
<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>วัดระดับความเสี่ยงการลงทุน</title>
    <style>
        body { font-family: Arial, sans-serif; margin: 40px; text-align: center; }
        form { max-width: 400px; margin: auto; text-align: left; }
        label, select, button { display: block; margin-top: 10px; width: 100%; }
        button { padding: 10px; background-color: #28a745; color: white; border: none; cursor: pointer; }
        button:hover { background-color: #218838; }
        #result { margin-top: 20px; font-size: 18px; font-weight: bold; }
    </style>
</head>
<body>

    <h2>แบบทดสอบวัดระดับความเสี่ยงการลงทุน</h2>
    
    <form id="riskForm">
        <label>คุณสามารถรับความเสี่ยงขาดทุนได้แค่ไหน?</label>
        <select id="riskLevel">
            <option value="ต่ำ">รับได้น้อยมาก (ต้องการความปลอดภัยสูง)</option>
            <option value="ปานกลาง">รับได้เล็กน้อย (ขาดทุนได้ไม่เกิน 5-10%)</option>
            <option value="สูง">รับได้สูง (พร้อมรับความเสี่ยงมาก)</option>
        </select>

        <button type="button" onclick="analyzeRisk()">วิเคราะห์ความเสี่ยง</button>
    </form>

    <div id="result"></div>

    <script>
        function analyzeRisk() {
            var riskLevel = document.getElementById("riskLevel").value;
            var recommendation = "";

            if (riskLevel === "ต่ำ") {
                recommendation = "📉 แนะนำ: กองทุนตราสารหนี้, อสังหาริมทรัพย์";
            } else if (riskLevel === "ปานกลาง") {
                recommendation = "📊 แนะนำ: หุ้นพื้นฐานดี, กองทุนผสม";
            } else if (riskLevel === "สูง") {
                recommendation = "🚀 แนะนำ: หุ้นเทคโนโลยี, คริปโตเคอเรนซี";
            }

            document.getElementById("result").innerHTML = "ผลลัพธ์: " + recommendation;
        }
    </script>

</body>
</html>
