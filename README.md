const dupontd = [
    { name: "Dupont", sex: "m" },
    { name: "DUPONT", sex: "m" },
    { name: "duPont", sex: "f" },
    { name: "dupond", sex: "f" }
];


function foreach(t,fx){
    for(let v of t){
        fx(v);
    }
}

function trans(t, fx) {
   let passed = [];
   for (let v of t){
       passed.push(fx(v))}
       return passed;
}

function setNom({name,sex}){
    sex == 'm' ? name = `Monsieur ${name}` : name = `Madame ${name}`
    return { name }
}

function upperCase(pers) {
    pers.name = pers.name.toUpperCase();
}

let ok=  trans(dupontd ,setNom);
let ko=  foreach(dupontd ,upperCase);
