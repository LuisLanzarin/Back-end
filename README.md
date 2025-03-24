const express = require('express');
const cors = require('cors');

const app = express();
app.use(express.json());
app.use(cors());

const personalTrainers = [
    { id: 1, nome: "João", latitude: -23.5505, longitude: -46.6333, especialidade: "Musculação" },
    { id: 2, nome: "Maria", latitude: -23.5587, longitude: -46.6358, especialidade: "Pilates" }
];

app.get('/api/trainers', (req, res) => {
    res.json(personalTrainers);
});

app.listen(5000, () => console.log("API rodando na porta 5000"));
