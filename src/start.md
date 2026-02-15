<style>

.start-container  {
    font-size:1.4em;
    text-align:center;
}

.revisit {
    font-size:2em;
    background: linear-gradient(45deg, gold, green);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

.link {
    background: linear-gradient(90deg, #0b5394, purple);
    color: #fff!important;
    border-radius:20pt;
    padding:0 10pt 2pt 10pt;
    text-decoration:none!important;
    display:inline-block;
}
.link:hover {
    background: linear-gradient(270deg, #0b5394, purple);
    border-bottom: 2px dashed #1d655e;
    text-decoration:none!important;
}

.download {
    border-bottom: 2px dashed #1d655e;
    font-weight: 700;
    color:#fff!important;
}

.download:hover {
    border-bottom: 2px dashed #fff;
}

#download-tar-gz {color:#fff;}

.stripes {
    background-image: 
        repeating-linear-gradient(
            to right,
            rgba(0, 0, 0, 0.05),
            rgba(0, 0, 0, 0.25) 24px,
            transparent 2px,
            transparent 10px
        ),
        radial-gradient(circle at top center, rgba(255, 255, 255, 0.15) 0%, transparent 60%),
        linear-gradient(to right, gold, green);
    
    background-blend-mode: overlay;
    border-radius:20pt;
    padding:10pt;
}

.blur {
    backdrop-filter:blur(8px);
    border:1pt solid rgba(255,255,255,.2);
    box-shadow: var(--tw-inset-shadow), var(--tw-inset-ring-shadow), var(--tw-ring-offset-shadow), var(--tw-ring-shadow), var(--tw-shadow);
    --tw-shadow: 0 25px 50px -12px var(--tw-shadow-color, #00000040);
    }
</style>
<script>
async function getLatestReleaseTag() {
    const url = "https://api.github.com/repos/plans-coding/immer-in-bewegung/releases/latest";

    try {
        const response = await fetch(url);
        if (!response.ok) {
            throw new Error(`HTTP error! status: ${response.status}`);
        }
        const data = await response.json();
        //console.log(data.tag_name);
        document.getElementById('download-zip').innerHTML = "Download latest version " + data.tag_name + " (zip)";
        document.getElementById('download-zip').href = "https://github.com/plans-coding/immer-in-bewegung/archive/refs/tags/" + data.tag_name + ".zip";
        document.getElementById('download-tar-gz').href = "https://github.com/plans-coding/immer-in-bewegung/archive/refs/tags/" + data.tag_name + ".tar.gz";
        return data.tag_name;
    } catch (error) {
        console.error("Error fetching latest release:", error);
    }
}

// Call the function
getLatestReleaseTag();

</script>
<br>
<div class="start-container">
    <img src="img/frog.svg" style="height:150pt;">
        <h1 class="revisit">Revisit your travel memories</h1>
        <p>Open source travel documentation app for self-hosting or serverless usage<br><b>Lightweight and future proof</b></p>
        <p><br>Try out the online version using <a class="link" href="https://online.bewegung.app/">example data</a> or <a class="link" href="https://online.bewegung.app/?path=source">your own data</a>.</p>
    <br>

<div class="stripes">
<div style="display:flex;">
    <div class="blur" style="display:flex;align-items: center;justify-content: center;bbackground-color:var(--sidebar-bg);border-radius:30pt;padding:0 20pt 0 20pt;margin:auto;flex-wrap:wrap;">
        <img style="display:block;" src="https://rust-lang.org/static/images/rust-logo-blk.svg" alt="Rust" height="100">
        <img style="display:block;" src="https://webassembly.org/css/webassembly.svg" alt="WebAssembly" height="60">&nbsp;&nbsp;&nbsp;
        <img style="display:block;" src="img/sqlite.svg" alt="SQLite" height="65">
    </div>
</div>

<p>For self-hosting deployment</p>

<a class="download" id="download-zip" style="text-decoration:none;" href="https://github.com/plans-coding/immer-in-bewegung/releases/latest/" target="_blank" rel="noopener noreferrer">Download latest version (zip)</a><br />

<a id="download-tar-gz" style="text-decoration:none;" href="https://github.com/plans-coding/immer-in-bewegung/releases/latest/" target="_blank" rel="noopener noreferrer">Download in other format (tar.gz)</a>
</div>

</div>
