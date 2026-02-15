# SOUFIANE
document.getElementById("predictionForm").addEventListener("submit", function(e) {
    e.preventDefault();

    let grade = document.getElementById("grade").value;
    let hours = document.getElementById("hours").value;
    let absences = document.getElementById("absences").value;

    let result = "";

    if (grade >= 12 && hours >= 10 && absences < 5) {
        result = "Performance élevée ✅";
    } else if (grade >= 10) {
        result = "Performance moyenne ⚠️";
    } else {
        result = "Risque d’échec ❌";
    }

    document.getElementById("result").innerHTML =
        "<h3>Résultat : " + result + "</h3>";
});

