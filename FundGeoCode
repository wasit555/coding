#Code No.1
                                                                                             #Wasit Khampeerapakorn 6230479321
x = input()  #รับข้อมูลที่ต้องการแปลงเป็นRLEมา
x += 'S' #เพิ่มตัวแปรที่เข้าไว้ปิดท้ายเข้ามาเพิ่อขยายขอบเขตในการวนลูปในบรรทัดที่5
n = 1 #กำหนดตัวแปรนับตัวซ้ำ
out = '' #กำหนดตัวแปรสำหรับเก็บข้อมูลและเตรียมส่งออก
for i in range(1,len(x)) : #คำสั่งวนลูปตั้งแต่ตัวที่2จนถึงตัวก่อนสุดท้าย เริ่มโดยการหยิบตัวที่2มาเปรียบเทียบกับตัวที่ก่อนหน้าไปเรื่อยๆจนถึงตัวก่อนสุดท้าย ในที่นี้ตัวที่ถูกเพิ่มจากตอนแรก'S'จะไม่ถูกนำมาเช็ค
    if x[i-1] == x[i]: # ถ้าตัวที่2เหมือนตัวแรกจะไปเพิ่ม1หน่วยในตัวแปรนับและวนลูปต่อไป
        n += 1
    else:
        out += str(n) + str(x[i-1]) #ถ้าตัวที่2ไม่เหมือนตัวแรกจะทำการจัดเก็บข้อมูลและจำนวนที่ซ้ำกันโดยให้จำนวนบอกความถี่ที่ซ้ำขึ้นก่อน
        n = 1 #resetตัวแปรนับตัวซ้ำแล้วเริ่มวนลูปตัวถัดไปในบรรทัดที่5
 print(out) #ทำการแสดงข้อมูลจากตัวแปรเก็บข้อมูล
 
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

#Code No.2
                                                                                                   #Wasit Khampeerapakorn 6230479321
Data = str(input())                #รับข้อมูลครั้งที่ 1 เข้ามาแล้วเก็บในตัวแปรData
#Ex. 0 0 2 2 0 0 2 2 0 0 2 2 0 0 2 2 2 2 0 0 0 0 0 0 0 0 3 3 0 0 2 0 0 0 0 0 0 0 0 0 2 2 0 0 0 2 2 2 0 0 3 3 3 3 0 0 0 0 3 3 2 2 0 0
x = []                             #สร้างตัวแปรxมาเก็บข้อมูลที่ผ่านการแก้ไขการจัดเรียง
for i in range(0,len(Data)) :      #นำตัวแปรDataมาลูปเพื่อกำจัดช่องว่างและเก็บข้อมูลในตัวแปรxในรูปของListโดยข้อมูลแต่ละตัวจะถูกกำหนดตำแหน่งตั้งแต่0-63
    if Data[i] != ' ' or '':
        x += Data[i]
want = str(input())                #รับข้อมูลครั้งที่ 2 ที่ต้องการทราบตำแหน่งแบบQuadtrees
#Ex. 2 หรือ 3    
out = ''                           #สร้างตัวแปรเพื่อใช้ในการส่งข้อมูลออก

##2                                #ขั้นตอนนี้เป็นการCheck layerนอกสุดที่ละQuadrantแบบQuadtree(4x4)
if x[0] != '0' and x[0:4]==x[8:12]==x[16:20]==x[24:28]==[want]*4 :     #ถ้าตัวแรกไม่เท่ากับ0และตัวที่0-3,8-11,16-19,24-27และตัวข้อมูลที่ต้องการทราบตำแหน่งเหมือนกัน
    out += " + (2,A)"                                                  #จะทำการเก็บข้อมูลในรูปแบบQuadtreesในตัวแปร out
if x[4] != '0' and x[4:8]==x[12:16]==x[20:24]==x[28:32]==[want]*4 :
    out += " + (2,B)"
if x[32] != '0' and x[32:36]==x[40:44]==x[48:52]==x[56:60]==[want]*4 :
    out += " + (2,D)"
if x[36] != '0' and x[36:40]==x[44:48]==x[52:56]==x[60:64]==[want]*4 :
    out += " + (2,C)"
     
##1                                #ขั้นตอนนี้เป็นการCheck layerชั้นรองลงมา(2x2)
#Ax                                #ทำการCheck 4Quadrantย่อยของ 4Quadrantใหญ่แบบQuadtrees
if x[0] != '0' and x[0:2]==x[8:10]==[want]*2 :                         #ถ้าตัวแรกไม่เท่ากับ0และตัวที่0-1,8-9และตัวข้อมูลที่ต้องการทราบตำแหน่งเหมือนกัน
    if " + (2,A)" not in out :                                         #codeนี้เป็นการกันไม่ให้เก็บข้อมูลทับกับLayerนอกสุด
        out += " + (1,AA)"                                             #จะทำการเก็บข้อมูลในรูปแบบQuadtreesในตัวแปร out
if x[2] != '0' and x[2:4]==x[10:12]==[want]*2 :
     if " + (2,A)" not in out :
        out += " + (1,AB)"
if x[16] != '0' and x[16:18]==x[24:26]==[want]*2 :
    if " + (2,A)" not in out :
        out += " + (1,AD)"
if x[18] != '0' and x[18:20]==x[26:28]==[want]*2 :
     if " + (2,A)" not in out :
        out += " + (1,AC)"
#Bx
if x[4] != '0' and x[4:6]==x[12:14]==[want]*2 :
     if " + (2,B)" not in out :
        out += " + (1,BA)"
if x[6] != '0' and x[6:8]==x[14:16]==[want]*2 :
    if " + (2,B)" not in out :
        out += " + (1,BB)"
if x[20] != '0' and x[20:22]==x[28:30]==[want]*2 :
    if " + (2,B)" not in out :
        out += " + (1,BD)"
if x[22] != '0' and x[22:24]==x[30:32]==[want]*2 :
    if " + (2,B)" not in out :
        out += " + (1,BC)"
#Dx
if x[32] != '0' and x[32:34]==x[40:42]==[want]*2 :
    if " + (2,D)" not in out :
        out += " + (1,DA)"
if x[34] != '0' and x[34:36]==x[42:44]==[want]*2 :
    if " + (2,D)" not in out :
        out += " + (1,DB)"
if x[48] != '0' and x[48:50]==x[56:58]==[want]*2 :
    if " + (2,D)" not in out :
        out += " + (1,DD)"
if x[50] != '0' and x[50:52]==x[58:60]==[want]*2 :
    if " + (2,D)" not in out :
        out += " + (1,DC)"
#Cx
if x[36] != '0' and x[36:38]==x[44:46]==[want]*2 :
    if " + (2,C)" not in out :
        out += " + (1,CA)"
if x[38] != '0' and x[38:40]==x[46:48]==[want]*2 :
    if " + (2,C)" not in out :
        out += " + (1,CB)"
if x[52] != '0' and x[52:54]==x[60:62]==[want]*2 :
    if " + (2,C)" not in out :
        out += " + (1,CD)"
if x[54] != '0' and x[54:56]==x[62:64]==[want]*2 :
    if " + (2,C)" not in out :
        out += " + (1,CC)"
    
##0                                  #ขั้นตอนนี้เป็นการCheck layerชั้นในสุด(1 pixel)
#AAx                                 #ทำการCheck 4Quadrantย่อยในสุดของ 4Quadrantย่อยแบบQuadtrees
if x[0] == want :                    #ถ้าตัวแรกและตัวข้อมูลที่ต้องการทราบตำแหน่งเหมือนกัน
    if " + (1,AA)" not in out :      #codeนี้เป็นการกันไม่ให้เก็บข้อมูลทับกับLayer(2x2)
        out += " + (0,AAA)"          #จะทำการเก็บข้อมูลในรูปแบบQuadtreesในตัวแปร out
if x[1] == want :
    if " + (1,AA)" not in out :
        out += " + (0,AAB)"
if x[8] == want :
    if " + (1,AA)" not in out :
        out += " + (0,AAD)"
if x[9] == want :
    if " + (1,AA)" not in out :
        out += " + (0,AAC)"
#ABx
if x[2] == want :
    if " + (1,AB)" not in out :
        out += " + (0,ABA)"
if x[3] == want :
    if " + (1,AB)" not in out :
        out += " + (0,ABB)"
if x[10] == want :
    if " + (1,AB)" not in out :
        out += " + (0,ABD)"
if x[11] == want :
    if " + (1,AB)" not in out :
        out += " + (0,ABC)"
#ADx
if x[16] == want :
    if " + (1,AD)" not in out :
        out += " + (0,ADA)"
if x[17] == want :
    if " + (1,AD)" not in out :
        out += " + (0,ADB)"
if x[24] == want :
    if " + (1,AD)" not in out :
        out += " + (0,ADD)"
if x[25] == want :
    if " + (1,AD)" not in out :
        out += " + (0,ADC)"
#ACx      
if x[18] == want :
    if " + (1,AC)" not in out :
        out += " + (0,ACA)"
if x[19] == want :
    if " + (1,AC)" not in out :
        out += " + (0,ACB)"
if x[26] == want :
    if " + (1,AC)" not in out :
        out += " + (0,ACD)"
if x[27] == want :
    if " + (1,AC)" not in out :
        out += " + (0,ACC)"
#BAx
if x[4] == want :
    if " + (1,BA)" not in out :
        out += " + (0,BAA)"
if x[5] == want :
    if " + (1,BA)" not in out :
        out += " + (0,BAB)"
if x[12] == want :
    if " + (1,BA)" not in out :
        out += " + (0,BAD)"
if x[13] == want :
    if " + (1,BA)" not in out :
        out += " + (0,BAC)"
#BBx
if x[6] == want :
    if " + (1,BB)" not in out :
        out += " + (0,BBA)"
if x[7] == want :
    if " + (1,BB)" not in out :
        out += " + (0,BBB)"
if x[14] == want :
    if " + (1,BB)" not in out :
        out += " + (0,BBD)"
if x[15] == want :
    if " + (1,BB)" not in out :
        out += " + (0,BBC)"
#BDx
if x[20] == want :
    if " + (1,BD)" not in out :
        out += " + (0,BDA)"
if x[21] == want :
    if " + (1,BD)" not in out :
        out += " + (0,BDB)"
if x[28] == want :
    if " + (1,BD)" not in out :
        out += " + (0,BDD)"
if x[29] == want :
    if " + (1,BD)" not in out :
        out += " + (0,BDC)"
#BCx
if x[22] == want :
    if " + (1,BC)" not in out :
        out += " + (0,BCA)"
if x[23] == want :
    if " + (1,BC)" not in out :
        out += " + (0,BCB)"
if x[30] == want :
    if " + (1,BC)" not in out :
        out += " + (0,BCD)"
if x[31] == want :
    if " + (1,BC)" not in out :
        out += " + (0,BCC)"
#DAx
if x[32] == want :
    if " + (1,DA)" not in out :
        out += " + (0,DAA)"
if x[33] == want :
    if " + (1,DA)" not in out :
        out += " + (0,DAB)"
if x[40] == want :
    if " + (1,DA)" not in out :
        out += " + (0,DAD)"
if x[41] == want :
    if " + (1,DA)" not in out :
        out += " + (0,DAC)"
#DBx
if x[34] == want :
    if " + (1,DB)" not in out :
        out += " + (0,DBA)"
if x[35] == want :
    if " + (1,DB)" not in out :
        out += " + (0,DBB)"
if x[42] == want :
    if " + (1,DB)" not in out :
        out += " + (0,DBD)"
if x[43] == want :
    if " + (1,DB)" not in out :
        out += " + (0,DBC)"
#DDx
if x[48] == want :
    if " + (1,DD)" not in out :
        out += " + (0,DDA)"
if x[49] == want :
    if " + (1,DD)" not in out :
        out += " + (0,DDB)"
if x[56] == want :
    if " + (1,DD)" not in out :
        out += " + (0,DDD)"
if x[57] == want :
    if " + (1,DD)" not in out :
        out += " + (0,DDC)"
#DCx        
if x[50] == want :
    if " + (1,DC)" not in out :
        out += " + (0,DCA)"
if x[51] == want :
    if " + (1,DC)" not in out :
        out += " + (0,DCB)"
if x[58] == want :
    if " + (1,DC)" not in out :
        out += " + (0,DCD)"
if x[59] == want :
    if " + (1,DC)" not in out :
        out += " + (0,DCC)"
#CAx
if x[36] == want :
    if " + (1,CA)" not in out :
        out += " + (0,CAA)"
if x[37] == want :
    if " + (1,CA)" not in out :
        out += " + (0,CAB)"
if x[44] == want :
    if " + (1,CA)" not in out :
        out += " + (0,CAD)"
if x[45] == want :
    if " + (1,CA)" not in out :
        out += " + (0,CAC)"
#CBx
if x[38] == want :
    if " + (1,CB)" not in out :
        out += " + (0,CBA)"
if x[39] == want :
    if " + (1,CB)" not in out :
        out += " + (0,CBB)"
if x[46] == want :
    if " + (1,CB)" not in out :
        out += " + (0,CBD)"
if x[47] == want :
    if " + (1,CB)" not in out :
        out += " + (0,CBC)"
#CDx
if x[52] == want :
    if " + (1,CD)" not in out :
        out += " + (0,CDA)"
if x[53] == want :
    if " + (1,CD)" not in out :
        out += " + (0,CDB)"
if x[60] == want :
    if " + (1,CD)" not in out :
        out += " + (0,CDD)"
if x[61] == want :
    if " + (1,CD)" not in out :
        out += " + (0,CDC)"
#CCx        
if x[54] == want :
    if " + (1,CC)" not in out :
        out += " + (0,CCA)"
if x[55] == want :
    if " + (1,CC)" not in out :
        out += " + (0,CCB)"
if x[62] == want :
    if " + (1,CC)" not in out :
        out += " + (0,CCD)"
if x[63] == want :
    if " + (1,CC)" not in out :
        out += " + (0,CCC)"

out = out[3:]                       #ทำการจัดรูปในตัวแปรoutใหม่เพื่อลบเครื่องหมาย"+"ที่เกินมา
print("Final Tree = " + out)        #ทำการแสดงผลที่เก็บในตัวแปรoutพร้อมกับคำว่า"Final Tree = "
