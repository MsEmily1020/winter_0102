## ๐ป ์๋ฃ ์ํ๊ธฐ ํ๋ก๊ทธ๋จ GUI
- ํด๋น ์๋ฃ์ ํด๋ฆญ ํ ๊ธ์ก ํฌ์ํ์ฌ ๊ฑฐ์ค๋ฆ๋ ๋ฐ ์๋ฃ ๋ฐ๊ธฐ

## โ Project execution period
  - 2022.01.02

## ๐  Development Environment
- MVC (๋ชจ๋ธ-๋ทฐ-์ปจํธ๋กค๋ฌ, modelโviewโcontroller) ์ด์ฉ
- GUI
  
  - Language : `Java 8` 
  - JDK `1.8.0_341`
  - Tool : `Eclipse`

## ๐ Main Composition
- GridLayout ์ค์ 
- ์ ํ ์ ํ ํ๋ฉด(ํด๋ฆญ ์ ํด๋น ์ ํ ๋ฐฐ๊ฒฝํ๋ฉด ์ ๋ณ๊ฒฝ)
  ```java
    lb.setIcon(icon); //์์ด์ฝ ์ค์ 
	lb.setText(Integer.toString(vo.getPrice()) + "์"); //๊ธ์ก ๋ณด์ด๊ธฐ
	lb.setHorizontalTextPosition(JLabel.CENTER);
	lb.setVerticalTextPosition(JLabel.BOTTOM);
	lb.setHorizontalAlignment(JLabel.CENTER);
			
	lb.setOpaque(true); //๋ผ๋ฒจ ๋ฐฐ๊ฒฝ์ ์ค์  ํ  ์ ์๋๋ก
	lb.setBackground(Color.white); //๊ธฐ๋ณธ ์ ํ์
    lbList.add(lb);
  
    MouseEvent e...
    if((JLabel)e.getSource == lbList.get(i))
      e.getSource.setBackground(Color.red); //์ ํ ์ ํด๋น ๋ผ๋ฒจ ๋ฐฐ๊ฒฝ์์ ๋นจ๊ฐ
  ```
- ๊ฑฐ์ค๋ฆ๋
  ```java
    int money = Integer.parseInt(insertTf.getText()); //์๋ ฆ๊ฐ(ํฌ์ํ ๋)
	if(vo.getPrice() <= money) {
		JOptionPane.showMessageDialog(null, "๊ฑฐ์ค๋ฆ๋ : " + (money - vo.getPrice()));
		lbResult.setIcon(new ImageIcon("images/" + vo.getImageName() + ".jpg")); //ํด๋น ์ด๋ฏธ์ง ์ถ๋ ฅ
	}
	else
		JOptionPane.showMessageDialog(null, vo.getPrice() - money + "์์ด ๋ถ์กฑํฉ๋๋ค.");
  ```
