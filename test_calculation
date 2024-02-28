import calculate_volume

def test_calculate_sphere():
    result = calculate_volume.calculate_sphere(3)
    assert result == 113.112

def test_main(monkeypatch, capsys):
    # Define a function to simulate multiple user inputs
    user_inputs = ["4.67"]

    def mock_input(_):
        return user_inputs.pop(0)

    # Use the function to simulate user input
    monkeypatch.setattr('builtins.input', mock_input)

    # Call the main function, which uses input() and prints the result
    calculate_volume.main()

    # Capture the printed output
    captured = capsys.readouterr()
    assert captured.out.strip() == "Isipadu sfera = 426.67"
