<%*
let article = await tp.system.prompt("Enter the article (le, la, un, une, etc):");
let word = await tp.system.prompt("Enter the French noun:");
let meaning = await tp.system.prompt("Enter the English meaning:");
let gender = await tp.system.suggester(["Masculine", "Feminine"], ["m", "f"]);
let color = (gender === "m") ? "blue" : "pink";
let helpNote = (gender === "m") ? "[[💙 Masculine Help]]" : "[[🩷 Feminine Help]]";
tR += `- <span style="color:${color}">${article} ${word}</span> – ${meaning} ${helpNote}`;
%>
