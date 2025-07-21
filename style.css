{\rtf1\ansi\ansicpg1252\cocoartf2580
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fswiss\fcharset0 Helvetica;\f1\fnil\fcharset134 PingFangSC-Regular;}
{\colortbl;\red255\green255\blue255;}
{\*\expandedcolortbl;;}
\paperw11900\paperh16840\margl1440\margr1440\vieww11520\viewh8400\viewkind0
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0

\f0\fs24 \cf0 function visaSida(id) \{\
    document.querySelectorAll('.sida').forEach(s => s.classList.remove('aktiv'));\
    document.getElementById(id).classList.add('aktiv');\
\}\
\
const form = document.getElementById('recension-form');\
const lista = document.getElementById('recension-lista');\
\
function h\'e4mtaRecensioner() \{\
    return JSON.parse(localStorage.getItem('recensioner')) || [];\
\}\
\
function sparaRecensioner(recensioner) \{\
    localStorage.setItem('recensioner', JSON.stringify(recensioner));\
\}\
\
function renderaRecensioner() \{\
    lista.innerHTML = '';\
    const recensioner = h\'e4mtaRecensioner();\
    recensioner.reverse().forEach(rec => \{\
        const div = document.createElement('div');\
        div.className = 'recension';\
        div.innerHTML = `\
            <h3>$\{rec.namn\}</h3>\
            <div class="stj\'e4rnor">$\{'
\f1 \'a1\'ef
\f0 '.repeat(rec.betyg)\}$\{'
\f1 \'a1\'ee
\f0 '.repeat(5 - rec.betyg)\}</div>\
            <p>$\{rec.text\}</p>\
        `;\
        lista.appendChild(div);\
    \});\
\}\
\
form.addEventListener('submit', function(e) \{\
    e.preventDefault();\
\
    const namn = document.getElementById('spel-namn').value.trim();\
    const text = document.getElementById('recension-text').value.trim();\
    const betyg = parseInt(document.getElementById('betyg').value);\
\
    if (namn && text && betyg) \{\
        const recensioner = h\'e4mtaRecensioner();\
        recensioner.push(\{ namn, text, betyg \});\
        sparaRecensioner(recensioner);\
        renderaRecensioner();\
        form.reset();\
        visaSida('hem');\
    \}\
\});\
\
renderaRecensioner();\
}