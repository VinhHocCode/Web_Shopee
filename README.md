Các cách căn giữa trong CSS

- Cách 1: dùng
  text-align: center;
  line-height: 100px; (đưa chữ ra giữa thẻ cha)
  => Khi chỉ có đúng 1 thẻ con (thẻ heading, p, span) thì dùng thẳng vào các thẻ đó
  => Khi có nhiều thẻ con thì dùng vào thẻ chứa tất cả thẻ con (thẻ cha)

- Cách 2: dùng
  display: flex; (cho thẻ cha)
  margin: auto; (cho thẻ con)

- Cách 3: dùng
  display: flex;
  align-items: center; (căn theo chiều dọc trục cross axis)
  justify-content: center; (căn theo chiều ngang trục main axis)

- Cách 4: dùng
  position: relative; (cho thẻ cha)

  position: absolute; (cho thẻ con)
  top: 50%; (50% của thẻ chứa nó, không căn ra giữa)
  left: 50%; (ra giữa màn hình và vẫn bị lệch)
  transform: translate(-50%, -50%); (ăn theo chính nó để căn ra giữa)

Fallback Image

- thẻ img thêm attribute onerror=""
  <img onerror="this.src='link ảnh mới'" src="link ảnh" alt="">

- thẻ div thêm url mới vào background-image
  background-image: url('link ảnh'), url('link ảnh mới');

Tối ưu sử dụng hình ảnh trên trang web

1. Sử dụng định dạng ảnh phù hợp

   - Hình học, vector, ...: SVG
   - Bitmap transparent: PNG, WEBP
   - Bitmap không transparent: JPEG, WEBP

2. Nén hình ảnh (giảm dung lượng)
   https://tinypng.com/
3. Sử dụng kích thước ảnh phù hợp

   - Original: 4000px x 4000px,
     Figma: 800px x 800px (CSS),
     Resize 1600px x 1600px (2x),
     đáp ứng tốt cho cả màn hình PPI/DPI cao (retina)
   - PPI (Pixel per inch: bao gồm màn hình),
     DPi (Dots per inch: bao gồm cả màn hình và in ấn): 100 DPI, 300 DPI thì 300 có mật độ cao hơn
     mặc dù tính trên cùng 1 đơn vị diện tích
     nên 300 có nhiều điểm ảnh hơn

Loại màn hình:

1. Màn hình thường (DPI thấp - 1:1): 800px x 800px ✅, 1600px x 1600px ❌
2. Màn hình retina (DPI cao 2:1): 800px x 800px ❌, 1600px x 1600px ✅

Ngày bắt đầu khóa học HTML & CSS:
Ngày kết thúc khóa học HTML & CSS: 12/1/2026
