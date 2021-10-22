<%* 
selection = tp.file.selection();
cursor = tp.file.cursor(0);
const highlightr = await tp.system.suggester(["🍓 Red","🍊 Orange","🌼 Yellow","🍏 Aqua","🌿 Green","🦋 Blue","🦄 Purple","🐰 Grey"],["red","orange","yellow","aqua", "green","blue","purple","grey"]);
return "<mark class='" + highlightr + "'>" + selection + cursor + "</mark><%tp.file.cursor(1)%>";
%>