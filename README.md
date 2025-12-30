using UnityEngine;
using UnityEngine.SceneManagement;

public class GameManager : MonoBehaviour
{
    public static GameManager instance;
    public int score = 0;

    void Awake()
    {
        instance = this;
    }

    public void AddScore(int value)
    {
        score += value;
        Debug.Log("Score: " + score);
    }

    public void GameOver()
    {
        
        SceneManager.LoadScene(SceneManager.GetActiveScene().buildIndex);
    }
}
