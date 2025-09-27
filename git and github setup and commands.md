<svg width="600" height="200" xmlns="http://www.w3.org/2000/svg">
  <rect x="10" y="20" width="140" height="40" fill="#E0F7FA" stroke="#00838F"/>
  <text x="20" y="45" font-family="sans-serif" font-size="14">Working Directory</text>

  <rect x="200" y="20" width="140" height="40" fill="#FFF8E1" stroke="#FFA000"/>
  <text x="210" y="45" font-family="sans-serif" font-size="14">Staging Area (Index)</text>

  <rect x="390" y="20" width="160" height="40" fill="#E8F5E9" stroke="#388E3C"/>
  <text x="400" y="45" font-family="sans-serif" font-size="14">Local Repository (HEAD)</text>

  <rect x="250" y="110" width="160" height="40" fill="#F3E5F5" stroke="#6A1B9A"/>
  <text x="260" y="135" font-family="sans-serif" font-size="14">Remote Repository</text>

  <!-- Arrows -->
  <line x1="150" y1="40" x2="200" y2="40" stroke="#000" marker-end="url(#arrow)"/>
  <line x1="340" y1="40" x2="390" y2="40" stroke="#000" marker-end="url(#arrow)"/>
  <line x1="470" y1="60" x2="470" y2="110" stroke="#000" marker-end="url(#arrow)"/>

  <defs>
    <marker id="arrow" viewBox="0 0 10 10" refX="5" refY="5"
            markerWidth="6" markerHeight="6" orient="auto-start-reverse">
      <path d="M0,0 L10,5 L0,10 Z" fill="#000"/>
    </marker>
  </defs>

  <!-- Labels on arrows -->
  <text x="160" y="30" font-family="sans-serif" font-size="12">git add</text>
  <text x="325" y="30" font-family="sans-serif" font-size="12">git commit</text>
  <text x="480" y="85" font-family="sans-serif" font-size="12">git push</text>
</svg>
