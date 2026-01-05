// ตัวอย่างข้อมูลผู้สมัคร
const data = {
    "chiangmai": [
        {district:"เขต 1", candidate:"นาย ก", party:"พรรค X", photo:"https://via.placeholder.com/50"},
        {district:"เขต 2", candidate:"นาง ข", party:"พรรค Y", photo:"https://via.placeholder.com/50"}
    ],
    "bangkok": [
        {district:"เขต 1", candidate:"นาย ค", party:"พรรค Z", photo:"https://via.placeholder.com/50"},
        {district:"เขต 2", candidate:"นาง ง", party:"พรรค W", photo:"https://via.placeholder.com/50"}
    ],
    "songkhla": [
        {district:"เขต 1", candidate:"นาย ญ", party:"พรรค A", photo:"https://via.placeholder.com/50"},
        {district:"เขต 2", candidate:"นาง ฎ", party:"พรรค B", photo:"https://via.placeholder.com/50"}
    ]
};

const popup = document.getElementById("popup");

// เมื่อโหลด SVG
document.getElementById("map").addEventListener("load", function() {
    const svgDoc = this.contentDocument;
    const provinces = svgDoc.querySelectorAll(".province");

    provinces.forEach(p => {
        p.addEventListener("click", e => {
            const id = e.target.id;
            const items = data[id];
            let html = "";
            if(items){
                html += "<strong>จังหวัด: " + id.charAt(0).toUpperCase() + id.slice(1) + "</strong><br>";
                items.forEach(i => {
                    html += i.district + " - " + i.candidate + " (" + i.party + ")<br>";
                    html += '<img src="'+i.photo+'" alt="'+i.candidate+'"><br>';
                });
            } else {
                html = "<strong>จังหวัด: " + id.charAt(0).toUpperCase() + id.slice(1) + "</strong><br>ยังไม่มีข้อมูล";
            }
            popup.innerHTML = html;
            popup.style.display = "block";
            popup.style.left = (e.pageX + 10) + "px";
            popup.style.top = (e.pageY + 10) + "px";
        });
    });
});

// ปิด popup ถ้าคลิกพื้นที่ว่าง
document.addEventListener("click", e => {
    if(!e.target.classList.contains("province")){
        popup.style.display = "none";
    }
});
