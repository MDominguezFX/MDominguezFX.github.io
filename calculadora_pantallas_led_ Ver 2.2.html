<html lang="es">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Calculadora de Pantallas LED</title>
<style>
  body { font-family: Arial, sans-serif; max-width: 600px; margin: 2em auto; padding: 0 1em; text-align: center; }
  h1 { text-align: center; }
  label { display: block; margin-top: 1em; font-weight: bold; }
  select, input { width: 100%; padding: 0.5em; margin-top: 0.3em; font-size: 1em; }
  button { margin-top: 1.5em; padding: 0.75em; font-size: 1.1em; background: #f39c12; color: white; border: none; cursor: pointer; border-radius: 5px; }
  button:hover { background: #e67e22; }
  .result { margin-top: 2em; background: #f9f9f9; padding: 1em; border-radius: 8px; box-shadow: 0 0 5px #ccc; }
  .diagram { margin-top: 2em; text-align: center; display: flex; flex-direction: column; align-items: center; }
</style>
</head>
<body>

<h1>Calculadora de Pantallas LED</h1>

<label for="moduleType">Selecciona el modelo de pantalla:</label>
<select id="moduleType">
  <!-- OUTDOOR ordenados de menor a mayor pixel pitch -->
  <option value="P2.9 Outdoor">P2.9 OUTDOOR (500x1000 mm)</option>
  <option value="P5">P5 OUTDOOR (960x960 mm)</option>
  <option value="P6.66 Outdoor">P6.66 OUTDOOR (960x960 mm)</option>
  
  <!-- Indoor -->
  <option value="P3.03 Indoor">P3.03 Indoor (640x480 mm)</option>
  <option value="P1.8 Indoor">P1.8 Indoor (640x480 mm)</option>
  <option value="P4 Indoor 640x480">P4 Indoor (640x480 mm)</option>
  <option value="P4 Indoor 960x960">P4 Indoor (960x960 mm)</option>
</select>

<label for="width">Cantidad de módulos de ancho:</label>
<input type="number" id="width" min="1" step="1" value="3" />

<label for="height">Cantidad de módulos de alto:</label>
<input type="number" id="height" min="1" step="1" value="2" />

<button id="calculateBtn">Calcular</button>

<div class="result" id="result" style="display:none;"></div>
<div class="diagram" id="diagram" style="display:none;"></div>

<script>
  const moduleConfigs = {
    "P2.9 Outdoor": {
      moduleWidthMm: 500,
      moduleHeightMm: 1000,
      pixelPitchMm: 2.9,
      powerConsumptionW: 240,
    },
    "P5": {
      moduleWidthMm: 960,
      moduleHeightMm: 960,
      pixelPitchMm: 5,
      powerConsumptionW: 250,
    },
    "P6.66 Outdoor": {
      moduleWidthMm: 960,
      moduleHeightMm: 960,
      pixelPitchMm: 6.66,
      powerConsumptionW: 280,
    },
    "P3.03 Indoor": {
      moduleWidthMm: 640,
      moduleHeightMm: 480,
      pixelPitchMm: 3.03,
      powerConsumptionW: 180,
    },
    "P1.8 Indoor": {
      moduleWidthMm: 640,
      moduleHeightMm: 480,
      pixelPitchMm: 1.8,
      powerConsumptionW: 220,
    },
    "P4 Indoor 640x480": {
      moduleWidthMm: 640,
      moduleHeightMm: 480,
      pixelPitchMm: 4,
      powerConsumptionW: 150,
    },
    "P4 Indoor 960x960": {
      moduleWidthMm: 960,
      moduleHeightMm: 960,
      pixelPitchMm: 4,
      powerConsumptionW: 200,
    },
  };

  function ledScreenCalculator(widthModules, heightModules, moduleType) {
    if (!moduleConfigs[moduleType]) {
      throw new Error("Tipo de módulo inválido");
    }

    const config = moduleConfigs[moduleType];
    const totalModules = widthModules * heightModules;
    const totalPowerConsumption = totalModules * config.powerConsumptionW;
    const amperes = (totalPowerConsumption / 220).toFixed(2);

    const adjustedWidthMm = widthModules * config.moduleWidthMm;
    const adjustedHeightMm = heightModules * config.moduleHeightMm;

    const adjustedWidthM = adjustedWidthMm / 1000;
    const adjustedHeightM = adjustedHeightMm / 1000;

    const totalPixelsWidth = adjustedWidthMm / config.pixelPitchMm;
    const totalPixelsHeight = adjustedHeightMm / config.pixelPitchMm;

    return {
      totalModules,
      adjustedWidthM: Number(adjustedWidthM.toFixed(2)),
      adjustedHeightM: Number(adjustedHeightM.toFixed(2)),
      totalPixelsWidth: Math.round(totalPixelsWidth),
      totalPixelsHeight: Math.round(totalPixelsHeight),
      totalPowerConsumption: Math.round(totalPowerConsumption),
      amperes,
    };
  }

  function drawDiagram(widthModules, heightModules, moduleWidth, moduleHeight) {
    const diagramDiv = document.getElementById("diagram");
    const canvasWidth = widthModules * moduleWidth / 10;
    const canvasHeight = heightModules * moduleHeight / 10;

    const canvas = document.createElement("canvas");
    canvas.width = canvasWidth + 50; // Extra space for labels
    canvas.height = canvasHeight + 50; // Extra space for labels
    const ctx = canvas.getContext("2d");

    // Background color
    ctx.fillStyle = "#D3D3D3";
    ctx.fillRect(0, 0, canvas.width, canvas.height);

    // Modules
    ctx.fillStyle = "#B0B0B0";
    for (let i = 0; i < widthModules; i++) {
      for (let j = 0; j < heightModules; j++) {
        ctx.strokeStyle = "#000";
        ctx.lineWidth = 1;
        ctx.strokeRect(i * moduleWidth / 10 + 25, j * moduleHeight / 10 + 25, moduleWidth / 10, moduleHeight / 10);
        ctx.fillRect(i * moduleWidth / 10 + 25, j * moduleHeight / 10 + 25, moduleWidth / 10, moduleHeight / 10);
      }
    }

    // Width label
    ctx.fillStyle = "#000";
    ctx.font = "14px Arial";
    ctx.textAlign = "center";
    ctx.fillText(`${(widthModules * moduleWidth / 1000).toFixed(2)} m`, canvas.width / 2, canvas.height - 10);

    // Height label
    ctx.save();
    ctx.translate(10, canvas.height / 2);
    ctx.rotate(-Math.PI / 2);
    ctx.fillText(`${(heightModules * moduleHeight / 1000).toFixed(2)} m`, 0, 0);
    ctx.restore();

    diagramDiv.style.display = "block";
    diagramDiv.innerHTML = "<h2>Vista del plano:</h2>";
    diagramDiv.appendChild(canvas);
  }

  document.getElementById("calculateBtn").addEventListener("click", () => {
    const width = parseInt(document.getElementById("width").value);
    const height = parseInt(document.getElementById("height").value);
    const moduleType = document.getElementById("moduleType").value;
    const resultDiv = document.getElementById("result");

    if (isNaN(width) || width <= 0 || isNaN(height) || height <= 0) {
      alert("Por favor ingresa cantidades válidas mayores que cero.");
      return;
    }

    try {
      const result = ledScreenCalculator(width, height, moduleType);
      const config = moduleConfigs[moduleType];

      let recommendation = "";

      if (result.totalModules > 6) {
        const phaseAmps = (result.amperes / 3).toFixed(2);
        recommendation = `
          <p><strong>Consumo por fase (trifásico):</strong> ${phaseAmps} A</p>
          <p><strong>Sugerencia:</strong> Use una llave térmica de al menos ${Math.ceil(result.amperes * 1.5)} A para manejar el consumo inicial.</p>
        `;
      }

      resultDiv.style.display = "block";
      resultDiv.innerHTML = `
        <h2>Resultados:</h2>
        <p><strong>Modelo:</strong> ${moduleType}</p>
        <p><strong>Total de módulos:</strong> ${result.totalModules}</p>
        <p><strong>Dimensiones ajustadas:</strong> ${result.adjustedWidthM} m x ${result.adjustedHeightM} m</p>
        <p><strong>Resolución total (píxeles):</strong> ${result.totalPixelsWidth} x ${result.totalPixelsHeight}</p>
        <p><strong>Consumo total de energía:</strong> ${result.totalPowerConsumption} W (${result.amperes} A)</p>
        ${recommendation}
      `;

      drawDiagram(width, height, config.moduleWidthMm, config.moduleHeightMm);
    } catch (err) {
      alert(err.message);
    }
  });
</script>

</body>
</html>
