import os
from bs4 import BeautifulSoup

BASE_DIR = "../temp/duqe-1-1"  # 티스토리 백업 풀어놓은 최상위 폴더

for folder in os.listdir(BASE_DIR):
    folder_path = os.path.join(BASE_DIR, folder)
    if not os.path.isdir(folder_path):
        continue
    
    #폴더 안의 html 파일 찾기
    html_files = [f for f in os.listdir(folder_path) if f.endswith(".html")]
    if not html_files:
        continue

    html_path = os.path.join(folder_path, html_files[0])

    with open(html_path, "r", encoding="utf-8") as f:
        soup = BeautifulSoup(f, "html.parser")

    # 날짜 추출 (티스토리 HTML 구조에 맞게 selector 수정 필요)
    date_tag = soup.select_one(".date")  # 예: <span class="date">2025.09.05</span>
    if not date_tag:
        continue

    raw_date = date_tag.get_text(strip=True)  # "2025.09.05"
    date_only = raw_date.split()[0]

    # 기본 폴더명
    new_folder_name = date_only

    new_folder_path = os.path.join(BASE_DIR, new_folder_name)
    # 중복 처리: 이미 존재하면 -1, -2 붙이기
    suffix = 1
    while os.path.exists(new_folder_path):
        new_folder_name = f"{date_only}-{suffix}"
        new_folder_path = os.path.join(BASE_DIR, new_folder_name)
        suffix += 1

    # 실제 변경
    os.rename(folder_path, new_folder_path)
    print(f"{folder} → {new_folder_name} 변경 완료")
