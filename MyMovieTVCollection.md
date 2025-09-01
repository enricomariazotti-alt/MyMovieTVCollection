---
title: My Movie & TV Collection
layout: default
nav_order: 99
---

# My Movie & TV Collection (Blu-ray and DVD) 🎬📀

<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Movie Collection</title>
<style>
  :root{
    --bg: #ffffff;
    --text: #111827; /* slate-900 */
    --muted-text: #374151; /* gray-700 */
    --border: #e5e7eb; /* gray-200 */
    --th-bg: #f3f4f6; /* gray-100 */
    --th-text: #111827;
    --row-alt: #fafafa;
    --link: #2563eb;
    --focus: #93c5fd;
  }
  @media (prefers-color-scheme: dark){
    :root{
      --bg: #0b0f17;
      --text: #e5e7eb; /* gray-200 */
      --muted-text: #9ca3af; /* gray-400 */
      --border: #1f2937; /* gray-800 */
      --th-bg: #111827; /* slate-900 */
      --th-text: #f9fafb; /* near-white */
      --row-alt: #0f172a; /* slate-900 deeper */
      --link: #60a5fa;
      --focus: #2563eb;
    }
  }
  /* Support Jekyll themes that toggle via data-theme="dark" */
  body[data-theme="dark"]{
    --bg: #0b0f17;
    --text: #e5e7eb;
    --muted-text: #9ca3af;
    --border: #1f2937;
    --th-bg: #111827;
    --th-text: #f9fafb;
    --row-alt: #0f172a;
    --link: #60a5fa;
    --focus: #2563eb;
  }

  body{ background: var(--bg); color: var(--text); }
  a{ color: var(--link); }

  .toolbar{ display:flex; gap:.75rem; align-items:center; margin:.5rem 0 1rem; flex-wrap:wrap; }
  .toolbar input[type="text"]{
    padding:.5rem .75rem; border:1px solid var(--border); border-radius:.5rem; width: min(700px, 100%);
    background: transparent; color: var(--text);
  }
  .toolbar input[type="text"]:focus{ outline: 2px solid var(--focus); outline-offset:2px; }

  table { border-collapse: collapse; width: 100%; font-size: .95rem; }
  thead th {
    background: var(--th-bg);
    color: var(--th-text);
    position: sticky; top: 0; z-index: 1;
  }
  th, td { border: 1px solid var(--border); padding: 8px; text-align: left; }
  tbody tr:nth-child(even){ background: var(--row-alt); }

  img { max-width: 120px; max-height: 170px; width: auto; height: auto; border-radius:.25rem; border:1px solid var(--border); }

  /* Collapsible groups */
  .group-toggle{ cursor:pointer; display:inline-flex; align-items:center; gap:.5rem; font-weight:600; }
  .caret{ display:inline-block; transition: transform .2s ease; }
  .caret[aria-expanded="true"]{ transform: rotate(90deg); }
  tr.child{ display:none; }
  tr.child.show{ display: table-row; }
  .child .title{ padding-left: 1.5rem; color: var(--muted-text); font-weight: 500; }
  .mono{ font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace; }
  .nowrap{ white-space: nowrap; }
</style>
</head>
<body>

<div class="toolbar">
  <input type="text" id="searchInput" onkeyup="filterTable()" placeholder="Search title, barcode, year…">
  <label class="mono"><input type="checkbox" id="onlyGroups" onchange="filterTable()"> show only groups</label>
</div>

<table id="movieTable">
<thead>
<tr>
<th>Title</th>
<th>Barcode</th>
<th>Year</th>
<th class="nowrap">N. of Discs</th>
<th>Img link</th>
</tr>
</thead>
<tbody>
  <!-- GROUP: Batman Trilogy -->
  <tr class="group" data-group="batman">
    <td>
      <button class="group-toggle" data-target="batman" aria-expanded="false" aria-controls="batman-rows">
        <span class="caret" aria-hidden="true">▶</span> Batman – The Dark Knight Trilogie
      </button>
    </td>
    <td>5051889001751</td><td>2012</td><td>5</td>
    <td><img alt="Batman Trilogy" src="https://www.icollecteverything.com/images/movie/main/240/2405304_1.jpg"></td>
  </tr>
  <tr id="batman-rows" class="child" data-parent="batman">
    <td class="title">Disc 1 — Batman Begins (2005)</td>
    <td class="mono">—</td><td>2005</td><td>1</td><td>—</td>
  </tr>
  <tr class="child" data-parent="batman">
    <td class="title">Disc 2 — The Dark Knight (2008)</td>
    <td class="mono">—</td><td>2008</td><td>1</td><td>—</td>
  </tr>
  <tr class="child" data-parent="batman">
    <td class="title">Disc 3 — The Dark Knight Rises (2012)</td>
    <td class="mono">—</td><td>2012</td><td>1</td><td>—</td>
  </tr>
  <tr class="child" data-parent="batman">
    <td class="title">Disc 4 — Bonus / Special Features</td>
    <td class="mono">—</td><td>—</td><td>1</td><td>—</td>
  </tr>
  <tr class="child" data-parent="batman">
    <td class="title">Disc 5 — Bonus / Special Features</td>
    <td class="mono">—</td><td>—</td><td>1</td><td>—</td>
  </tr>

  <!-- GROUP: Cars 1–3 -->
  <tr class="group" data-group="cars">
    <td>
      <button class="group-toggle" data-target="cars" aria-expanded="false" aria-controls="cars-rows">
        <span class="caret" aria-hidden="true">▶</span> Cars 1–3 (3-Disc Set)
      </button>
    </td>
    <td>8717418519995</td><td>2017</td><td>3</td>
    <td><img alt="Cars 1–3" src="https://www.icollecteverything.com/images/movie/main/248/2488617_1.jpg"></td>
  </tr>
  <tr id="cars-rows" class="child" data-parent="cars">
    <td class="title">Disc 1 — Cars (2006)</td>
    <td class="mono">—</td><td>2006</td><td>1</td><td>—</td>
  </tr>
  <tr class="child" data-parent="cars">
    <td class="title">Disc 2 — Cars 2 (2011)</td>
    <td class="mono">—</td><td>2011</td><td>1</td><td>—</td>
  </tr>
  <tr class="child" data-parent="cars">
    <td class="title">Disc 3 — Cars 3 (2017)</td>
    <td class="mono">—</td><td>2017</td><td>1</td><td>—</td>
  </tr>

  <!-- GROUP: Dexter Collection (seasons & spin-offs) -->
  <tr class="group" data-group="dexter">
    <td>
      <button class="group-toggle" data-target="dexter" aria-expanded="false" aria-controls="dexter-rows">
        <span class="caret" aria-hidden="true">▶</span> Dexter — Collection
      </button>
    </td>
    <td class="mono">—</td><td>2010–2025</td><td>?</td>
    <td><img alt="Dexter" src="https://www.icollecteverything.com/images/movie/main/223/2237802_1.jpg"></td>
  </tr>
  <tr id="dexter-rows" class="child" data-parent="dexter">
    <td class="title">Season 1</td>
    <td>4010884238082</td><td>2012</td><td>4</td><td><img src="https://www.icollecteverything.com/images/movie/main/223/2237802_1.jpg" alt="Dexter S1"></td>
  </tr>
  <tr class="child" data-parent="dexter">
    <td class="title">Season 2</td>
    <td>4010884238099</td><td>2012</td><td>4</td><td><img src="https://www.icollecteverything.com/images/movie/main/223/2237804_1.jpg" alt="Dexter S2"></td>
  </tr>
  <tr class="child" data-parent="dexter">
    <td class="title">Season 3</td>
    <td>4010884238105</td><td>2011</td><td>4</td><td><img src="https://www.icollecteverything.com/images/movie/main/155/1555125_1.jpg" alt="Dexter S3"></td>
  </tr>
  <tr class="child" data-parent="dexter">
    <td class="title">Season 4</td>
    <td>4010884238112</td><td>2010</td><td>4</td><td><img src="https://www.icollecteverything.com/images/movie/main/102/1022859_1.jpg" alt="Dexter S4"></td>
  </tr>
  <tr class="child" data-parent="dexter">
    <td class="title">Season 5</td>
    <td>4010884238129</td><td>2012</td><td>4</td><td><img src="https://www.icollecteverything.com/images/movie/main/129/1291438_1.jpg" alt="Dexter S5"></td>
  </tr>
  <tr class="child" data-parent="dexter">
    <td class="title">Season 6</td>
    <td>4010884238136</td><td>2013</td><td>4</td><td><img src="https://www.icollecteverything.com/images/movie/main/223/2237800_1.jpg" alt="Dexter S6"></td>
  </tr>
  <tr class="child" data-parent="dexter">
    <td class="title">Season 7</td>
    <td>4010884288148</td><td>2012</td><td>4</td><td><img src="https://www.icollecteverything.com/images/movie/main/155/1555100_1.jpg" alt="Dexter S7"></td>
  </tr>
  <tr class="child" data-parent="dexter">
    <td class="title">New Blood — The Complete Series</td>
    <td>7333018022874</td><td>2021</td><td>4</td><td><img src="https://www.icollecteverything.com/images/movie/main/277/2776978_1.jpg" alt="Dexter New Blood"></td>
  </tr>
  <tr class="child" data-parent="dexter">
    <td class="title">Original Sin</td>
    <td>191329281215</td><td>2025</td><td>1</td><td><img src="https://www.icollecteverything.com/images/movie/main/321/3215647_1.jpg" alt="Dexter Original Sin"></td>
  </tr>

  <!-- Single titles (unchanged) -->
  <tr><td>Baymax - Riesiges Robowabohu</td><td>8717418454111</td><td>2014</td><td>1</td><td><img src="https://www.icollecteverything.com/images/movie/main/195/1957543_1.jpg" alt="Baymax"></td></tr>
  <tr><td>Captain America: The First Avenger</td><td>4010884250886</td><td>2011</td><td>2</td><td><img src="https://www.icollecteverything.com/images/movie/main/119/1199372_1.jpg" alt="CA First Avenger"></td></tr>
  <tr><td>Der gestiefelte Kater</td><td>5053083167899</td><td>2011</td><td>1</td><td><img src="https://www.icollecteverything.com/images/movie/main/316/3160293_1.jpg" alt="Puss in Boots"></td></tr>
  <tr><td>Drachenzähmen Leicht Gemacht 1-3</td><td>5053083188269</td><td>2019</td><td>3</td><td><img src="https://www.icollecteverything.com/images/movie/main/316/3163610_1.jpg" alt="HTTYD 1-3"></td></tr>
  <tr><td>Guardians of the Galaxy 1</td><td>8717418444266</td><td>2014</td><td>1</td><td><img src="https://www.icollecteverything.com/images/movie/main/164/1646483_1.jpg" alt="GOTG"></td></tr>
  <tr><td>Happy Feet</td><td>7321983000331</td><td>2006</td><td>1</td><td><img src="https://www.icollecteverything.com/images/movie/main/83/833145_1.jpg" alt="Happy Feet"></td></tr>
  <tr><td>Ice Age 1-5, 5 s</td><td>8717418579357</td><td>2017</td><td>5</td><td><img src="https://www.icollecteverything.com/images/movie/main/260/2603488_1.jpg" alt="Ice Age"></td></tr>
  <tr><td>Ich – Einfach unverbesserlich / Minions – 6 Movie Collection</td><td>5053083270025</td><td>2024</td><td>6</td><td><img src="https://www.icollecteverything.com/images/movie/main/324/3244100_1.jpg" alt="Despicable Me Collection"></td></tr>
  <tr><td>Iron Man Trilogie [Blu-ray]</td><td>4010324039880</td><td>2014</td><td>3</td><td><img src="https://www.icollecteverything.com/images/movie/main/195/1959539_1.jpg" alt="Iron Man Trilogy"></td></tr>
  <tr><td>Jurassic Park L’intégrale</td><td>5053083252557</td><td>2015</td><td>6</td><td><img src="https://www.icollecteverything.com/images/movie/main/315/3155820_1.jpg" alt="Jurassic Park Collection"></td></tr>
  <tr><td>Marvel Return of the First Avenger</td><td>8717418429638</td><td>2014</td><td>1</td><td><img src="https://www.icollecteverything.com/images/movie/main/177/1779535_1.jpg" alt="CA Winter Soldier (DE title)"></td></tr>
  <tr><td>Marvels Agents Of S.H.I.E.L.D.</td><td>8717418456290</td><td>2013</td><td>6</td><td><img src="https://www.icollecteverything.com/images/movie/main/231/2311816_1.jpg" alt="Agents of SHIELD"></td></tr>
  <tr><td>Marvel’s Avengers 1 The Avengers</td><td>8717418355876</td><td>2012</td><td>1</td><td><img src="https://www.icollecteverything.com/images/movie/main/225/2254393_1.jpg" alt="Avengers"></td></tr>
  <tr><td>Matrix 1-3</td><td>5051890153715</td><td>2003</td><td>3</td><td><img src="https://www.icollecteverything.com/images/movie/main/165/1659877_1.jpg" alt="Matrix Trilogy"></td></tr>
  <tr><td>Minecraft</td><td>5051890340993</td><td>2025</td><td>1</td><td><img src="https://www.icollecteverything.com/images/movie/main/321/3216335_1.jpg" alt="Minecraft Movie"></td></tr>
  <tr><td>Shrek - Shrekologie 1-4</td><td>5053083146979</td><td>2014</td><td>4</td><td><img src="https://www.icollecteverything.com/images/movie/main/248/2488602_1.jpg" alt="Shrek 1-4"></td></tr>
  <tr><td>Thor</td><td>4010884259940</td><td>2011</td><td>1</td><td><img src="https://www.icollecteverything.com/images/movie/main/114/1145399_1.jpg" alt="Thor"></td></tr>
  <tr><td>Transformers - 5-Movie Collection</td><td>5053083171292</td><td>2017</td><td>5</td><td><img src="https://www.icollecteverything.com/images/movie/main/256/2566836_1.jpg" alt="Transformers Collection"></td></tr>
  <tr><td>Transformers One</td><td>5053083270070</td><td>2023</td><td>1</td><td><img src="https://www.icollecteverything.com/images/movie/main/320/3209993_1.jpg" alt="Transformers One"></td></tr>
</tbody>
</table>

<script>
function filterTable(){
  const q = (document.getElementById('searchInput').value || '').trim().toUpperCase();
  const onlyGroups = document.getElementById('onlyGroups').checked;
  const rows = Array.from(document.querySelectorAll('#movieTable tbody tr'));
  const groupRows = rows.filter(r => r.classList.contains('group'));
  const childRows = rows.filter(r => r.classList.contains('child'));

  // Reset visibility
  rows.forEach(r => r.style.display = '');

  // Text match across all cells
  const matches = (tr) => Array.from(tr.cells).some(td => (td.textContent || '').toUpperCase().includes(q));

  // Apply filters
  rows.forEach(tr => {
    if (onlyGroups && !tr.classList.contains('group')) tr.style.display = 'none';
    if (q && !matches(tr)) tr.style.display = 'none';
  });

  // If a group is visible but its children are hidden by search, ensure children matching query are shown and group is expanded
  groupRows.forEach(g => {
    const key = g.dataset.group;
    const kids = childRows.filter(c => c.dataset.parent === key);
    const anyKidVisibleByQuery = q && kids.some(k => (k.textContent || '').toUpperCase().includes(q));
    if (anyKidVisibleByQuery){
      // show the group row if hidden by only-groups mismatch
      g.style.display = '';
      setExpanded(key, true);
      kids.forEach(k => {
        if ((k.textContent || '').toUpperCase().includes(q)) k.style.display = '';
      });
    }
  });
}

function setExpanded(groupKey, expanded){
  const btn = document.querySelector(`.group-toggle[data-target="${groupKey}"]`);
  const kids = document.querySelectorAll(`tr.child[data-parent="${groupKey}"]`);
  if (!btn) return;
  btn.setAttribute('aria-expanded', expanded ? 'true' : 'false');
  kids.forEach(k => k.classList.toggle('show', expanded));
}

// Toggle handling
addEventListener('click', (e) => {
  const t = e.target.closest('.group-toggle');
  if (!t) return;
  const key = t.dataset.target;
  const expanded = t.getAttribute('aria-expanded') === 'true';
  setExpanded(key, !expanded);
});
</script>

<!--
NOTES FOR YOU (safe to leave in the md):
- Dark mode: uses prefers-color-scheme and also respects body[data-theme="dark"].
- Collapsible groups: add a parent <tr class="group" data-group="KEY"> then children <tr class="child" data-parent="KEY">.
- For Batman and Cars, disc titles are common defaults. Replace with exact disc names if your specific edition differs.
- To group more sets (e.g., Ice Age, Jurassic Park), replicate the pattern.
-->

</body>
</html>
