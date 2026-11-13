# AnamnesIA

Primera visita guiada en medicina estética. Aplicación web de un solo fichero.

**Usar la app:** https://fborrasumh.github.io/anamnesia/

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.24186888.svg)](https://doi.org/10.5281/zenodo.24186888)

**Idiomas:** español (por defecto), inglés, portugués; selector en la barra superior (o `?lang=en` / `?lang=pt` en la URL).

## Qué hace

Segunda app del [Kit EstéticIA](https://fborrasumh.github.io/kitesteticia/): la primera visita guiada de la consulta de medicina estética.

- **Paciente y técnicas**: identificador (no el nombre), edad, sexo, fototipo, peso y talla, motivo de consulta y las técnicas que se plantean entre diez: toxina botulínica, ácido hialurónico, bioestimuladores, hilos, peeling químico, mesoterapia y plasma rico en plaquetas, láser y luz pulsada, radiofrecuencia y ultrasonidos focalizados, criolipólisis y ácido desoxicólico.
- **Solo lo que importa**: las preguntas de los antecedentes cambian con las técnicas marcadas; seis se hacen siempre (embarazo, lactancia, infección en la zona, anticoagulantes y alergias).
- **Reglas fijas y explicadas**: cada respuesta se cruza con las contraindicaciones y precauciones habituales de cada técnica. Rojo es «no tratar ahora»; ámbar, «precaución». Cada aviso dice por qué.
- **Expectativas y cribado**: lo que espera el paciente y si es realista; cinco señales de alarma de trastorno dismórfico corporal basadas en los criterios del DSM-5 y el resultado de un cuestionario validado si se ha usado (por ejemplo, BDDQ-AS o COPS).
- **Datos que faltan**: la app avisa de lo que queda sin responder antes de dar el resultado por completo.
- **Resumen para la historia clínica** en Word o texto, y una **ficha JSON** (`kitesteticia-paciente/1`) para las siguientes apps del kit.

No usa IA y no hace ninguna llamada de red. Español, inglés y portugués.

## Privacidad

Todo se guarda en el navegador. Nada sale hacia ningún servidor. Se recomienda usar un identificador en lugar del nombre del paciente.

## Límites

Es una ayuda para médicos. Las reglas resumen contraindicaciones y precauciones habituales de fichas técnicas e instrucciones de uso; no recogen todas las posibles y manda la ficha técnica de cada producto. Las señales de alarma de trastorno dismórfico corporal no son un cuestionario validado y un cribado positivo no es un diagnóstico. No sustituye a la exploración ni al juicio clínico.

## Pruebas

`node tests/test_nucleo.js` (reglas, cribado, resumen y ficha) y `python3 tests/smoke.py` (recorrido completo en Chromium, tres idiomas, persistencia, accesibilidad WCAG 2.2 AA, CSP y móvil).

## Autoría

Fernando Borrás Rocher (Universidad Miguel Hernández de Elche) y Elena Caride Miana (Dra. Caride Medicina Estética & Antiaging).

Segunda app del Kit EstéticIA, diseñado para el alumnado del Máster de Formación Permanente en Medicina Estética Integral y Antienvejecimiento (UMH).

ORCID: Fernando Borrás Rocher [0000-0002-5519-4573](https://orcid.org/0000-0002-5519-4573) · Elena Caride Miana [0000-0002-7620-4857](https://orcid.org/0000-0002-7620-4857)

## Cómo citar

Borrás Rocher, F. y Caride Miana, E. (2026). *AnamnesIA* (v1.0.0) [Software]. DOI: [10.5281/zenodo.24186888](https://doi.org/10.5281/zenodo.24186888)

## Licencia

MIT. Véase [LICENSE](LICENSE).
