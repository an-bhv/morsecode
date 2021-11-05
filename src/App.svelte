<script>
import Ancmt from "./Ancmt.svelte";

let dcd = "";


const decode = (e) =>{
	const code = e.detail;
	dcd = code;
	fnc();
}

console.log(dcd);

let ans= [];

const fnc = () =>{
	
let ar = dcd.split(" / ");

for(let j = 0;j<ar.length;j++){

console.log(ar[j]);

let arr = ar[j].split(" ");

let s = "";

for(let i= 0;i<arr.length;i++){

	if(arr[i]==".-"){
		s+='a';
	}
	else if(arr[i]=="-..."){
		s+='b';
	}
	
	else if(arr[i]=="-.-."){
		s+='c';
	}
	else if(arr[i]=="-.."){
		s+='d';
	}
	else if(arr[i]=="."){
		s+='e';
	}
	else if(arr[i]=="..-."){
		s+='f';
	}
	else if(arr[i]=="--."){
		s+='g';
	}
	else if(arr[i]=="...."){
		s+='h';
	}
	else if(arr[i]==".."){
		s+='i';
	}
	else if(arr[i]==".---"){
		s+='j';
	}
	else if(arr[i]=="-.-"){
		s+='k';
	}
	else if(arr[i]==".-.."){
		s+='l';
	}
	else if(arr[i]=="--"){
		s+='m';
	}
	else if(arr[i]=="-."){
		s+='n';
	}
	else if(arr[i]=="---"){
		s+='o';
	}
	else if(arr[i]==".--."){
		s+='p';
	}
	else if(arr[i]=="--.-"){
		s+='q';
	}
	else if(arr[i]==".-."){
		s+='r';
	}
	else if(arr[i]=="..."){
		s+='s';
	}
	else if(arr[i]=="-"){
		s+='t';
	}
	else if(arr[i]=="..-"){
		s+='u';
	}
	else if(arr[i]=="...-"){
		s+='v';
	}
	else if(arr[i]==".--"){
		s+='w';
	}
	else if(arr[i]=="-..-"){
		s+='x';
	}
	else if(arr[i]=="-.--"){
		s+='y';
	}
	else if(arr[i]=="--.."){
		s+='z';
	}
	else if(arr[i]==".----"){
		s+='1';
	}
	else if(arr[i]=="..---"){
		s+='2';
	}
	else if(arr[i]=="...--"){
		s+='3';
	}
	else if(arr[i]=="....-"){
		s+='4';
	}
	else if(arr[i]=="....."){
		s+='5';
	}
	else if(arr[i]=="-...."){
		s+='6';
	}
	else if(arr[i]=="--..."){
		s+='7';
	}
	else if(arr[i]=="---.."){
		s+='8';
	}
	else if(arr[i]=="----."){
		s+='9';
	}
	else if(arr[i]=="-----"){
		s+='0';
	}
	else{
		s = "##INVALID INPUT##";
	}	
}

	ans.push(s);
	ans = ans;

}


console.log(ans);

}


</script>

<main>


	<h1>MORSE CODE TRANSLATOR</h1>

<Ancmt on:txt={decode}>

</Ancmt>
<h1>{dcd}</h1>
<p>
{#each ans as a}
	{a}
&nbsp;	
{/each}

</p>
</main>

<style>

main{
	text-align: center;
}

</style>