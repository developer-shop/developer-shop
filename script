const overlay = document.querySelector(".overlay");
const form  = document.querySelector("form"),
name = form.querySelector("#name"),
email = form.querySelector("#email"),
apk = form.querySelector("#apk"),
link = form.querySelector("#link"),      
msg = form.querySelector("#msg");

form.addEventListener("submit",(e)=>{
    e.preventDefault();
    submitForm(name.value, email.value, apk.value, link.value, msg.value)
})
 
function submitForm(name,email,apk,link,msg){
fetch("https://formsubmit.co/ajax/claroorlando773@gmail.com", {
    method: "POST",
    headers: { 
        'Content-Type': 'application/json',
        'Accept': 'application/json'
    },
    body: JSON.stringify({
        Name: name,
        Email: email,
        apk: apk,
        link: link,
        Message: msg;
        
    })
})
    .then(response => response.json())
    .then(data => {
        if (data.success == "true") {
            overlay.style.display="flex";
            overlay.addEventListener("click",()=>{
                overlay.style.display="none";
    
            })
            form.reset();
        }
    })
    .catch(error => console.log(error));
}
