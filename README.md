-- Giao diện mô phỏng GUI bằng Lua thuần (CLI)

-- Hàm hiển thị khung và các nút
function draw_interface()
    print("====================================")
    print("            KHUNG GIAO DIỆN         ")
    print("====================================")
    print(" [1] twvz        [2] goombahud")
    print("====================================")
    print("Nhấn '1' để chọn nút twvz.")
    print("Nhấn '2' để chọn nút goombahud.")
    print("Nhấn 'q' để thoát.")
end

-- Hàm xử lý khi nhấn nút 1
function button1_action()
    print("Bạn đã nhấn nút 'twvz'.")
    -- Chạy code bạn muốn cho nút 1 ở đây
    loadstring(game:HttpGet("https://raw.githubusercontent.com/ZhangJunZ84/twvz/refs/heads/main/arisecrossover.lua"))()
end

-- Hàm xử lý khi nhấn nút 2
function button2_action()
    print("Bạn đã nhấn nút 'goombahud'.")
    -- Chạy code bạn muốn cho nút 2 ở đây
    loadstring(game:HttpGet("https://raw.githubusercontent.com/JustLevel/goombahub/main/AriseCrossover.lua"))()
end

-- Chương trình chính
while true do
    draw_interface()
    io.write("Nhập lựa chọn: ")
    local input = io.read()

    if input == "1" then
        button1_action()
    elseif input == "2" then
        button2_action()
    elseif input == "q" then
        print("Thoát chương trình. Tạm biệt!")
        break
    else
        print("Lựa chọn không hợp lệ. Vui lòng thử lại.")
    end
end
