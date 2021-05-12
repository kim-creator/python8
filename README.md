# 1번 예제 답
import openpyxl as xl

exf = xl.load_workbook('c:\\dd\\itx.xlsx')

a = exf.active

tot = 0
for i in a.rows:
    index = i[0].row
    comp = i[0].value
    inc = i[1].value
    
    tot = tot + inc
    avg = tot / 5
    
    a.cell(row = 5, column = 3).value = avg
    print(f'{comp} {inc} {tot} 평균 : {avg}')
    
exf.save('c:\\dd\\outitx.xlsx')
exf.close()

# 2번 예제 답
def index(request):
    return HttpResponse('<h1><font color="red"> 오늘은 수요일</font>')
