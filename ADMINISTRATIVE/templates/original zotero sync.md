let fp = '';
if (data.creators && data.creators.length > 0) {
fp += data.creators[0]?.lastName;
if (data.creators.length == 2) {
	fp += '+';
	fp += data.creators[1]?.lastName;
} else if (data.creators.length > 2) {
	fp += '+';
}
if (data.date) {
	let year = new Date(data.date).getFullYear();
	fp += year.toString();
}
return 'References/' + fp;
}