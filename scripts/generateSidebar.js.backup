// /content/posts/를 순회해서 md데이터를 추출하여 _sidebar.md에 자동으로 목표을 생성하는 스크립트
// generateSidebar.js
const fs = require("fs");
const path = require("path");
const matter = require("gray-matter");

const ROOT = "content/posts";
const OUTPUT = "_sidebar.md";

const categories = [
  "Inspiration",
  "CaseStudy",
  "Notes",
  "Architecture",
  "Development",
  "Administration",
];

let sidebar = "* [홈](README.md)\n\n";
let categoryMap = {};

// Initialize category map
categories.forEach((cat) => {
  categoryMap[cat] = [];
});

// Traverse folders
function walk(dir) {
  const items = fs.readdirSync(dir);
  items.forEach((item) => {
    const fullPath = path.join(dir, item);
    const stat = fs.statSync(fullPath);
    if (stat.isDirectory()) {
      walk(fullPath);
    } else if (item.endsWith(".md")) {
      const content = fs.readFileSync(fullPath, "utf8");
      const { data } = matter(content);
      const category = data.category;
      const title = data.title || path.basename(item, ".md");
      const relativePath = fullPath.replace(/\\/g, "/");

      if (categoryMap[category]) {
        categoryMap[category].push({ title, path: relativePath });
      }
    }
  });
}

// Build sidebar content
function buildSidebar() {
  for (const cat of categories) {
    if (categoryMap[cat].length > 0) {
      sidebar += `* ${cat}\n`;
      categoryMap[cat].forEach((post) => {
        sidebar += `  * [${post.title}](${post.path})\n`;
      });
      sidebar += "\n";
    }
  }
}

// Run
walk(ROOT);
buildSidebar();
fs.writeFileSync(OUTPUT, sidebar);
console.log("✅ _sidebar.md 생성 완료!");
