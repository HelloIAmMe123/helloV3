<script>
function launch() {
    const target = "https://wingdemon.net";
    const win = window.open('about:blank', '_blank');

    win.document.body.style.margin = "0";
    win.document.body.style.height = "100vh";
    win.document.title = "Assignment Details"; 
    
    const link = win.document.createElement('link');
    link.rel = 'icon';
    link.href = 'https://gstatic.com';
    win.document.head.appendChild(link);

    const iframe = win.document.createElement('iframe');
    iframe.src = target;
    iframe.style.width = "100%";
    iframe.style.height = "100%";
    iframe.style.border = "none";
    iframe.allowFullscreen = true;

    win.document.body.appendChild(iframe);

    win.addEventListener('keydown', (e) => {
        if (e.key.toLowerCase() === "q") { win.close(); }
    });
}
</script>
