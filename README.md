while true do
    -- Langkah 1: Memulai (unload alat pancing)
    game.ReplicatedStorage.Msg.RemoteFunction:InvokeServer("装备卸载鱼竿")
    wait(1)

    -- Langkah 2: Melempar kail
    game.ReplicatedStorage.Msg.RemoteFunction:InvokeServer("抛竿", Vector3.new(-0.37, 0.00, 0.93))
    wait(1)

    -- Langkah 3: Goyangkan alat pancing secara terus menerus
    for i = 1, 10 do
        game.ReplicatedStorage.Msg.RemoteEvent:FireServer("摇晃鱼竿")
        wait(0.1)
    end

    -- Ulangi dari awal
end
