# equipo
para compañeros https://wokwi.com/projects/434261698802576385
```
[
    {
        "id": "7704709c0f325c10",
        "type": "tab",
        "label": "Proyecto",
        "disabled": false,
        "info": "",
        "env": []
    },
    {
        "id": "a4b716919b0b201d",
        "type": "mqtt in",
        "z": "7704709c0f325c10",
        "name": "",
        "topic": "Diplomadoequipo2",
        "qos": "2",
        "datatype": "auto-detect",
        "broker": "924a3888a2bded28",
        "nl": false,
        "rap": true,
        "rh": 0,
        "inputs": 0,
        "x": 150,
        "y": 420,
        "wires": [
            [
                "0b2f60b70df7886a"
            ]
        ]
    },
    {
        "id": "0b2f60b70df7886a",
        "type": "json",
        "z": "7704709c0f325c10",
        "name": "",
        "property": "payload",
        "action": "obj",
        "pretty": false,
        "x": 350,
        "y": 420,
        "wires": [
            [
                "747aa41e59253c1e",
                "b9edcaca61c59753",
                "a2fe63f7a8f7bf71",
                "a89de6efce9294c8",
                "ad033a0009a4eb82",
                "1fda2f6b2546b449",
                "fec1e44ac14f7f57",
                "28363c83d99173d5",
                "b76394122547bf59"
            ]
        ]
    },
    {
        "id": "747aa41e59253c1e",
        "type": "debug",
        "z": "7704709c0f325c10",
        "name": "debug 3",
        "active": false,
        "tosidebar": true,
        "console": false,
        "tostatus": false,
        "complete": "payload",
        "targetType": "msg",
        "statusVal": "",
        "statusType": "auto",
        "x": 520,
        "y": 420,
        "wires": []
    },
    {
        "id": "b9edcaca61c59753",
        "type": "function",
        "z": "7704709c0f325c10",
        "name": "VOLUMEN_ACTUAL",
        "func": "msg.payload = msg.payload.VOLUMENACTUAL;\nmsg.topic = \"VOLUMEN_ACTUAL\";\n\nreturn msg",
        "outputs": 1,
        "timeout": 0,
        "noerr": 0,
        "initialize": "",
        "finalize": "",
        "libs": [],
        "x": 600,
        "y": 320,
        "wires": [
            [
                "d7185535cf16783b",
                "d8154126c1194a9a",
                "d9bedcf673c4c0f4"
            ]
        ]
    },
    {
        "id": "d7185535cf16783b",
        "type": "ui_chart",
        "z": "7704709c0f325c10",
        "name": "",
        "group": "3952d9d26f321ea2",
        "order": 1,
        "width": 0,
        "height": 0,
        "label": "VOLUMEN ALMACENADO",
        "chartType": "line",
        "legend": "true",
        "xformat": "HH:mm:ss",
        "interpolate": "monotone",
        "nodata": "",
        "dot": false,
        "ymin": "0",
        "ymax": "50000",
        "removeOlder": 1,
        "removeOlderPoints": "",
        "removeOlderUnit": "3600",
        "cutout": 0,
        "useOneColor": false,
        "useUTC": false,
        "colors": [
            "#1f77b4",
            "#aec7e8",
            "#ff7f0e",
            "#2ca02c",
            "#98df8a",
            "#d62728",
            "#ff9896",
            "#9467bd",
            "#c5b0d5"
        ],
        "outputs": 1,
        "useDifferentColor": false,
        "className": "",
        "x": 860,
        "y": 280,
        "wires": [
            []
        ]
    },
    {
        "id": "d8154126c1194a9a",
        "type": "ui_gauge",
        "z": "7704709c0f325c10",
        "name": "",
        "group": "8fd08662e4d9affd",
        "order": 0,
        "width": 0,
        "height": 0,
        "gtype": "wave",
        "title": "VOLUMEN",
        "label": "L",
        "format": "{{value}}",
        "min": 0,
        "max": "50000",
        "colors": [
            "#00b500",
            "#e6e600",
            "#ca3838"
        ],
        "seg1": "",
        "seg2": "",
        "diff": false,
        "className": "",
        "x": 850,
        "y": 380,
        "wires": []
    },
    {
        "id": "a2fe63f7a8f7bf71",
        "type": "function",
        "z": "7704709c0f325c10",
        "name": "TEMPERATURA",
        "func": "msg.payload = msg.payload.TEMPERATURA;\nmsg.topic = \"TEMPERATURA\";\nreturn msg",
        "outputs": 1,
        "timeout": 0,
        "noerr": 0,
        "initialize": "",
        "finalize": "",
        "libs": [],
        "x": 610,
        "y": 520,
        "wires": [
            [
                "323e83b59e094bf8",
                "18e6ef7132eb4333",
                "fc7514eaf033bca9"
            ]
        ]
    },
    {
        "id": "a89de6efce9294c8",
        "type": "function",
        "z": "7704709c0f325c10",
        "name": "PH",
        "func": "msg.payload = msg.payload.PH;\nmsg.topic = \"PH\";\nreturn msg",
        "outputs": 1,
        "timeout": 0,
        "noerr": 0,
        "initialize": "",
        "finalize": "",
        "libs": [],
        "x": 570,
        "y": 620,
        "wires": [
            [
                "3594433c651ec453",
                "1dba1759d55c0682"
            ]
        ]
    },
    {
        "id": "8b40b0edf2e6f326",
        "type": "function",
        "z": "7704709c0f325c10",
        "name": "            AGITADOR",
        "func": "var agitador = Number(msg.payload.AGITADOR);\nvar mensaje = \"       AGITADOR\";\n\nif (agitador ==1) {\n    mensaje = \"      Activado.\";\n} else if (agitador==0) {\n    mensaje = \"           Desactivado\";\n}\n\nmsg.payload =mensaje;\nreturn msg",
        "outputs": 1,
        "timeout": 0,
        "noerr": 0,
        "initialize": "",
        "finalize": "",
        "libs": [],
        "x": 590,
        "y": 760,
        "wires": [
            [
                "fc57c23e0701f4ff"
            ]
        ]
    },
    {
        "id": "323e83b59e094bf8",
        "type": "ui_gauge",
        "z": "7704709c0f325c10",
        "name": "",
        "group": "452bdae8498581af",
        "order": 1,
        "width": 0,
        "height": 0,
        "gtype": "donut",
        "title": "TEMPERATURA DATOS",
        "label": "°C",
        "format": "{{value}}",
        "min": 0,
        "max": "80",
        "colors": [
            "#00b500",
            "#e6e600",
            "#ca3838"
        ],
        "seg1": "",
        "seg2": "",
        "diff": false,
        "className": "",
        "x": 910,
        "y": 560,
        "wires": []
    },
    {
        "id": "18e6ef7132eb4333",
        "type": "ui_chart",
        "z": "7704709c0f325c10",
        "name": "",
        "group": "3952d9d26f321ea2",
        "order": 0,
        "width": 0,
        "height": 0,
        "label": "TEMP-HUM",
        "chartType": "line",
        "legend": "true",
        "xformat": "HH:mm:ss",
        "interpolate": "monotone",
        "nodata": "",
        "dot": false,
        "ymin": "0",
        "ymax": "80",
        "removeOlder": 1,
        "removeOlderPoints": "",
        "removeOlderUnit": "3600",
        "cutout": 0,
        "useOneColor": false,
        "useUTC": false,
        "colors": [
            "#1f77b4",
            "#aa0808",
            "#ff7f0e",
            "#2ca02c",
            "#98df8a",
            "#d62728",
            "#ff9896",
            "#9467bd",
            "#c5b0d5"
        ],
        "outputs": 1,
        "useDifferentColor": false,
        "className": "",
        "x": 910,
        "y": 500,
        "wires": [
            []
        ]
    },
    {
        "id": "3594433c651ec453",
        "type": "ui_gauge",
        "z": "7704709c0f325c10",
        "name": "",
        "group": "452bdae8498581af",
        "order": 2,
        "width": 0,
        "height": 0,
        "gtype": "donut",
        "title": "pH",
        "label": "",
        "format": "{{value}}",
        "min": 0,
        "max": "14",
        "colors": [
            "#00b500",
            "#e6e600",
            "#ca3838"
        ],
        "seg1": "",
        "seg2": "",
        "diff": false,
        "className": "",
        "x": 910,
        "y": 600,
        "wires": []
    },
    {
        "id": "ad033a0009a4eb82",
        "type": "function",
        "z": "7704709c0f325c10",
        "name": "HUMEDAD",
        "func": "msg.payload = msg.payload.HUMEDAD;\nmsg.topic = \"HUMEDAD\";\nreturn msg",
        "outputs": 1,
        "timeout": 0,
        "noerr": 0,
        "initialize": "",
        "finalize": "",
        "libs": [],
        "x": 590,
        "y": 240,
        "wires": [
            [
                "18e6ef7132eb4333",
                "055781d2cc664eba"
            ]
        ]
    },
    {
        "id": "055781d2cc664eba",
        "type": "ui_gauge",
        "z": "7704709c0f325c10",
        "name": "",
        "group": "452bdae8498581af",
        "order": 1,
        "width": 0,
        "height": 0,
        "gtype": "donut",
        "title": "HUMEDAD DATOS",
        "label": "%",
        "format": "{{value}}",
        "min": 0,
        "max": "100",
        "colors": [
            "#ffeb0a",
            "#0fe600",
            "#050cd6"
        ],
        "seg1": "",
        "seg2": "",
        "diff": false,
        "className": "",
        "x": 890,
        "y": 200,
        "wires": []
    },
    {
        "id": "1fda2f6b2546b449",
        "type": "function",
        "z": "7704709c0f325c10",
        "name": "FLUJOENTRADA",
        "func": "msg.payload = msg.payload.FLUJOENTRADA;\nmsg.topic = \"FLUJOENTRADA\";\nreturn msg",
        "outputs": 1,
        "timeout": 0,
        "noerr": 0,
        "initialize": "",
        "finalize": "",
        "libs": [],
        "x": 610,
        "y": 840,
        "wires": [
            [
                "fa435bcad92b998f"
            ]
        ]
    },
    {
        "id": "fec1e44ac14f7f57",
        "type": "function",
        "z": "7704709c0f325c10",
        "name": "FLUJOSALIDA",
        "func": "msg.payload = msg.payload.FLUJOSALIDA;\nmsg.topic = \"FLUJOSALIDA\";\nreturn msg",
        "outputs": 1,
        "timeout": 0,
        "noerr": 0,
        "initialize": "",
        "finalize": "",
        "libs": [],
        "x": 600,
        "y": 920,
        "wires": [
            [
                "291c07ecc940f296"
            ]
        ]
    },
    {
        "id": "28363c83d99173d5",
        "type": "function",
        "z": "7704709c0f325c10",
        "name": "LIMITE",
        "func": "\nreturn msg;",
        "outputs": 1,
        "timeout": 0,
        "noerr": 0,
        "initialize": "",
        "finalize": "",
        "libs": [],
        "x": 600,
        "y": 1020,
        "wires": [
            [
                "e06191f0011ae3c7",
                "283165e507ba9e86"
            ]
        ]
    },
    {
        "id": "fa435bcad92b998f",
        "type": "ui_gauge",
        "z": "7704709c0f325c10",
        "name": "",
        "group": "8fd08662e4d9affd",
        "order": 1,
        "width": 0,
        "height": 0,
        "gtype": "compass",
        "title": "FLUJO ENTRADA",
        "label": "L/min",
        "format": "{{value}}",
        "min": 0,
        "max": "50",
        "colors": [
            "#00b500",
            "#e6e600",
            "#ca3838"
        ],
        "seg1": "",
        "seg2": "",
        "diff": false,
        "className": "",
        "x": 870,
        "y": 840,
        "wires": []
    },
    {
        "id": "291c07ecc940f296",
        "type": "ui_gauge",
        "z": "7704709c0f325c10",
        "name": "",
        "group": "8fd08662e4d9affd",
        "order": 2,
        "width": 0,
        "height": 0,
        "gtype": "compass",
        "title": "FLUJO SALIDA",
        "label": "Lmin",
        "format": "{{value}}",
        "min": 0,
        "max": "50",
        "colors": [
            "#00b500",
            "#e6e600",
            "#ca3838"
        ],
        "seg1": "",
        "seg2": "",
        "diff": false,
        "className": "",
        "x": 860,
        "y": 920,
        "wires": []
    },
    {
        "id": "ba956d1a7c86f32d",
        "type": "ui_text",
        "z": "7704709c0f325c10",
        "group": "dc8bf5de03b3595e",
        "order": 3,
        "width": "5",
        "height": "3",
        "name": "",
        "label": "NIVEL",
        "format": "{{msg.payload}}",
        "layout": "col-center",
        "className": "",
        "style": true,
        "font": "Lucida Sans Typewriter,Lucida Console,Monaco,monospace",
        "fontSize": "24",
        "color": "#ffffff",
        "x": 950,
        "y": 1020,
        "wires": []
    },
    {
        "id": "ef3b9ad86fb0b55d",
        "type": "ui_audio",
        "z": "7704709c0f325c10",
        "name": "ALERTA!! ",
        "group": "dc8bf5de03b3595e",
        "voice": "Google español",
        "always": true,
        "x": 960,
        "y": 1120,
        "wires": []
    },
    {
        "id": "fc57c23e0701f4ff",
        "type": "ui_text",
        "z": "7704709c0f325c10",
        "group": "dc8bf5de03b3595e",
        "order": 2,
        "width": "5",
        "height": "3",
        "name": "",
        "label": "AGITADOR",
        "format": "{{msg.payload}}",
        "layout": "col-center",
        "className": "",
        "style": true,
        "font": "Lucida Sans Typewriter,Lucida Console,Monaco,monospace",
        "fontSize": "24",
        "color": "#f8f7f7",
        "x": 930,
        "y": 720,
        "wires": []
    },
    {
        "id": "e06191f0011ae3c7",
        "type": "function",
        "z": "7704709c0f325c10",
        "name": "NIVEL",
        "func": "var nivel = Number(msg.payload.LIMITE);\nvar mensaje = \"\";\nif (nivel < 300 && nivel > 70) {\n    mensaje = \"Volumen en aumento o disminucion.\";\n} else if (nivel <= 70 && nivel >= 40) {\n    mensaje = \"Normal: El nivel del tanque es adecuado.\";\n} else if (nivel <= 39) {\n    mensaje = \"¡¡ALERTA!!! Exceso de volumen.\";\n    \n} else if (nivel >= 300 && nivel < 400) {\n    mensaje = \"Tanque vacío.\";\n}\n return{payload : mensaje}",
        "outputs": 1,
        "timeout": 0,
        "noerr": 0,
        "initialize": "",
        "finalize": "",
        "libs": [],
        "x": 770,
        "y": 1020,
        "wires": [
            [
                "ba956d1a7c86f32d"
            ]
        ]
    },
    {
        "id": "283165e507ba9e86",
        "type": "function",
        "z": "7704709c0f325c10",
        "name": "ALERTA",
        "func": "var nivel = Number(msg.payload.LIMITE);\nvar alerta = null;\nvar estadoAnterior = context.get(\"estadoAlerta\") || false;\n\nif (nivel <= 39 && !estadoAnterior) {\n    alerta = \"ALERTA: EXCESO DE VOLUMEN.\";\n    context.set(\"estadoAlerta\", true);  // Marca que ya alertó\n    return { payload: alerta };\n}\n\nif (nivel > 9 && estadoAnterior) {\n    context.set(\"estadoAlerta\", false);  // Se resetea si ya no está en condición de alerta\n}\n\nreturn null;",
        "outputs": 1,
        "timeout": 0,
        "noerr": 0,
        "initialize": "",
        "finalize": "",
        "libs": [],
        "x": 760,
        "y": 1120,
        "wires": [
            [
                "ef3b9ad86fb0b55d",
                "f1ff622fa4ace8ab"
            ]
        ]
    },
    {
        "id": "b04cb3bd3775b16a",
        "type": "ui_toast",
        "z": "7704709c0f325c10",
        "position": "dialog",
        "displayTime": "10",
        "highlight": "GREEN",
        "sendall": true,
        "outputs": 1,
        "ok": "OK",
        "cancel": "",
        "raw": false,
        "className": "",
        "topic": "WARNING",
        "name": "EXCESO DE VOLUMEN",
        "x": 1230,
        "y": 1220,
        "wires": [
            []
        ]
    },
    {
        "id": "f1ff622fa4ace8ab",
        "type": "change",
        "z": "7704709c0f325c10",
        "name": "",
        "rules": [
            {
                "t": "set",
                "p": "topic",
                "pt": "msg",
                "to": "LIMITE SUPERADO",
                "tot": "str"
            },
            {
                "t": "set",
                "p": "payload",
                "pt": "msg",
                "to": "VOLUMEN FUERA DE RANGO PERMITIDO",
                "tot": "str"
            }
        ],
        "action": "",
        "property": "",
        "from": "",
        "to": "",
        "reg": false,
        "x": 980,
        "y": 1220,
        "wires": [
            [
                "b04cb3bd3775b16a"
            ]
        ]
    },
    {
        "id": "81364793883b1020",
        "type": "change",
        "z": "7704709c0f325c10",
        "name": "",
        "rules": [
            {
                "t": "set",
                "p": "payload",
                "pt": "msg",
                "to": "VERIFICACION DE pH",
                "tot": "str"
            }
        ],
        "action": "",
        "property": "",
        "from": "",
        "to": "",
        "reg": false,
        "x": 820,
        "y": 660,
        "wires": [
            [
                "841ce359cb8c12da"
            ]
        ]
    },
    {
        "id": "841ce359cb8c12da",
        "type": "ui_toast",
        "z": "7704709c0f325c10",
        "position": "top right",
        "displayTime": "50",
        "highlight": "BLUE",
        "sendall": false,
        "outputs": 0,
        "ok": "OK",
        "cancel": "",
        "raw": false,
        "className": "",
        "topic": "COMBINACION DE COMPONENTES",
        "name": "MEDICION DE pH",
        "x": 1070,
        "y": 660,
        "wires": []
    },
    {
        "id": "b76394122547bf59",
        "type": "function",
        "z": "7704709c0f325c10",
        "name": "function 1",
        "func": "\nreturn msg;",
        "outputs": 1,
        "timeout": 0,
        "noerr": 0,
        "initialize": "",
        "finalize": "",
        "libs": [],
        "x": 380,
        "y": 720,
        "wires": [
            [
                "24ae8dbed9efb538",
                "8b40b0edf2e6f326"
            ]
        ]
    },
    {
        "id": "24ae8dbed9efb538",
        "type": "function",
        "z": "7704709c0f325c10",
        "name": "pH notificacion",
        "func": "\nif (msg.payload.AGITADOR==1) {\n    msg.payload = \"verificacion de pH\";\n\nreturn msg; }\nelse {\n    return null;\n}",
        "outputs": 1,
        "timeout": 0,
        "noerr": 0,
        "initialize": "",
        "finalize": "",
        "libs": [],
        "x": 600,
        "y": 700,
        "wires": [
            [
                "81364793883b1020"
            ]
        ]
    },
    {
        "id": "7444c526068ce1e4",
        "type": "telegram receiver",
        "z": "7704709c0f325c10",
        "name": "Receiver",
        "bot": "755a0f2cce857de2",
        "saveDataDir": "",
        "filterCommands": false,
        "x": 980,
        "y": 780,
        "wires": [
            [
                "ebebcd2fdcaae1e5"
            ],
            [
                "6488e6bd7881e1a0"
            ]
        ]
    },
    {
        "id": "0f191afbf8e85a1a",
        "type": "telegram sender",
        "z": "7704709c0f325c10",
        "name": "",
        "bot": "755a0f2cce857de2",
        "haserroroutput": false,
        "outputs": 1,
        "x": 1290,
        "y": 320,
        "wires": [
            []
        ]
    },
    {
        "id": "f6ee286e1fc0a498",
        "type": "telegram sender",
        "z": "7704709c0f325c10",
        "name": "",
        "bot": "755a0f2cce857de2",
        "haserroroutput": false,
        "outputs": 1,
        "x": 1450,
        "y": 500,
        "wires": [
            []
        ]
    },
    {
        "id": "6aa49be198022685",
        "type": "telegram sender",
        "z": "7704709c0f325c10",
        "name": "",
        "bot": "755a0f2cce857de2",
        "haserroroutput": false,
        "outputs": 1,
        "x": 1850,
        "y": 940,
        "wires": [
            []
        ]
    },
    {
        "id": "6488e6bd7881e1a0",
        "type": "debug",
        "z": "7704709c0f325c10",
        "name": "debug 1",
        "active": true,
        "tosidebar": true,
        "console": false,
        "tostatus": false,
        "complete": "false",
        "statusVal": "",
        "statusType": "auto",
        "x": 1260,
        "y": 920,
        "wires": []
    },
    {
        "id": "ebebcd2fdcaae1e5",
        "type": "function",
        "z": "7704709c0f325c10",
        "name": "function 3",
        "func": "let comando = msg.payload.content; // mensaje del usuario\nlet modo = \"\";\n\nswitch (comando.toLowerCase()) {\n\n    case \"volumen\":\n        modo = \"volumen\";\n        msg.payload = \" Enviando datos de volumen...\";\n        break;\n    case \"ph\":\n        modo = \"ph\";\n        msg.payload = \" Enviando datos de pH...\";\n        break;\n    case \"temperatura\":\n        modo = \"temperaura\";\n        msg.payload = \" Enviando datos de temperatura...\";\n        break;\n    case \"siguiente\":\n        modo = \"\";\n        msg.payload = \"Se detuvo elenvo. Esperando otro comando.\";\n        break;\n    default:\n        msg.payload = \" Comando no reconocdo. Usa: volumen, ph, temperatura o siguiente.\";\n}\n\nflow.set(\"modo\", modo); // guardamos en memoria el dato que se pidió\nreturn msg;",
        "outputs": 1,
        "timeout": 0,
        "noerr": 0,
        "initialize": "",
        "finalize": "",
        "libs": [],
        "x": 1420,
        "y": 840,
        "wires": [
            [
                "6aa49be198022685"
            ]
        ]
    },
    {
        "id": "d9bedcf673c4c0f4",
        "type": "function",
        "z": "7704709c0f325c10",
        "name": "filtro volumen",
        "func": "let modo = flow.get(\"modo\"); // modo guardado desde el comando Telegram\n\nif (modo === \"volumen\") {\n    let volumen = msg.payload; // VOLUMEN_ACTUAL entrega el valor directamente\n    msg.payload = ` VOLUMENACTUAL: ${volumen} ml`;\n    return msg;\n}\n\nreturn null; // No se envía nada si no está en modo \"volumen\"",
        "outputs": 1,
        "timeout": 0,
        "noerr": 0,
        "initialize": "",
        "finalize": "",
        "libs": [],
        "x": 990,
        "y": 320,
        "wires": [
            [
                "0f191afbf8e85a1a"
            ]
        ]
    },
    {
        "id": "fc7514eaf033bca9",
        "type": "function",
        "z": "7704709c0f325c10",
        "name": "filtro temp",
        "func": "let modo = flow.get(\"modo\"); // modo guardado desde el comando Telegram\n\nif (modo === \"temperatura\") {\n    let temperatura = msg.payload; // VOLUMEN_ACTUAL entrega el valor directamente\n    msg.payload = `TEMPERATURA: ${temperatura} C`;\n    return msg;\n}\n\nreturn null; // No se envía nada si no está en modo \"volumen\"",
        "outputs": 1,
        "timeout": 0,
        "noerr": 0,
        "initialize": "",
        "finalize": "",
        "libs": [],
        "x": 1200,
        "y": 500,
        "wires": [
            [
                "f6ee286e1fc0a498"
            ]
        ]
    },
    {
        "id": "9fd17378fc47685c",
        "type": "ui_toast",
        "z": "7704709c0f325c10",
        "position": "dialog",
        "displayTime": "3",
        "highlight": "",
        "sendall": true,
        "outputs": 1,
        "ok": "OK",
        "cancel": "",
        "raw": false,
        "className": "DEMASIADO ACIDO",
        "topic": "NO APTO PARA USO MEDICO",
        "name": "",
        "x": 1850,
        "y": 620,
        "wires": [
            []
        ]
    },
    {
        "id": "f64afa22e940f2f5",
        "type": "change",
        "z": "7704709c0f325c10",
        "name": "",
        "rules": [
            {
                "t": "set",
                "p": "payload",
                "pt": "msg",
                "to": "acidez ekevaadda",
                "tot": "str"
            }
        ],
        "action": "",
        "property": "",
        "from": "",
        "to": "",
        "reg": false,
        "x": 1680,
        "y": 620,
        "wires": [
            [
                "9fd17378fc47685c"
            ]
        ]
    },
    {
        "id": "1dba1759d55c0682",
        "type": "function",
        "z": "7704709c0f325c10",
        "name": "function 2",
        "func": "const valor = msg.payload;\nconst estabaFuera = context.get(\"fuera\") || false;\n\nif (valor < 1 || valor > 5) {\n    if (!estabaFuera) {\n        context.set(\"fuera\", true); // actualiza estado\n        msg.payload = ` Alerta: Valor fuera de rango: ${valor}`;\n        msg.topic = \"Alerta\";\n        return msg;\n    } else {\n        return null; // ya estaba fuera, no repite alerta\n    }\n} else {\n    context.set(\"fuera\", false); // vuelve al rango válido\n    return null; // no hay alerta si está en rango\n}",
        "outputs": 1,
        "timeout": 0,
        "noerr": 0,
        "initialize": "",
        "finalize": "",
        "libs": [],
        "x": 1460,
        "y": 700,
        "wires": [
            [
                "f64afa22e940f2f5"
            ]
        ]
    },
    {
        "id": "924a3888a2bded28",
        "type": "mqtt-broker",
        "name": "",
        "broker": "52.57.49.38",
        "port": 1883,
        "clientid": "",
        "autoConnect": true,
        "usetls": false,
        "protocolVersion": 4,
        "keepalive": 60,
        "cleansession": true,
        "autoUnsubscribe": true,
        "birthTopic": "",
        "birthQos": "0",
        "birthRetain": "false",
        "birthPayload": "",
        "birthMsg": {},
        "closeTopic": "",
        "closeQos": "0",
        "closeRetain": "false",
        "closePayload": "",
        "closeMsg": {},
        "willTopic": "",
        "willQos": "0",
        "willRetain": "false",
        "willPayload": "",
        "willMsg": {},
        "userProps": "",
        "sessionExpiry": ""
    },
    {
        "id": "3952d9d26f321ea2",
        "type": "ui_group",
        "name": "            GRAFICA",
        "tab": "a5f761beeff3491a",
        "order": 1,
        "disp": true,
        "width": "8",
        "collapse": false,
        "className": ""
    },
    {
        "id": "8fd08662e4d9affd",
        "type": "ui_group",
        "name": "LLENADO",
        "tab": "a5f761beeff3491a",
        "order": 4,
        "disp": true,
        "width": "6",
        "collapse": false,
        "className": ""
    },
    {
        "id": "452bdae8498581af",
        "type": "ui_group",
        "name": "                    DATOS",
        "tab": "a5f761beeff3491a",
        "order": 2,
        "disp": true,
        "width": 6,
        "collapse": false,
        "className": ""
    },
    {
        "id": "dc8bf5de03b3595e",
        "type": "ui_group",
        "name": "ALERTAS",
        "tab": "a5f761beeff3491a",
        "order": 3,
        "disp": true,
        "width": "5",
        "collapse": false,
        "className": ""
    },
    {
        "id": "755a0f2cce857de2",
        "type": "telegram bot",
        "botname": "EQUIPO2_JRH_DA_OJO_bot",
        "usernames": "",
        "chatids": "",
        "baseapiurl": "",
        "testenvironment": false,
        "updatemode": "polling",
        "pollinterval": 300,
        "usesocks": false,
        "sockshost": "",
        "socksprotocol": "socks5",
        "socksport": 6667,
        "socksusername": "anonymous",
        "sockspassword": "",
        "bothost": "",
        "botpath": "",
        "localbothost": "0.0.0.0",
        "localbotport": 8443,
        "publicbotport": 8443,
        "privatekey": "",
        "certificate": "",
        "useselfsignedcertificate": false,
        "sslterminated": false,
        "verboselogging": false
    },
    {
        "id": "a5f761beeff3491a",
        "type": "ui_tab",
        "name": "PREPARACION DE SOLUCIONES",
        "icon": "dashboard",
        "order": 1,
        "disabled": false,
        "hidden": false
    }
]

```
