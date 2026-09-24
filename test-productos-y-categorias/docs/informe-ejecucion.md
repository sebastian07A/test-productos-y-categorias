# Informe de ejecución de pruebas

## 1. Identificación

| Campo | Valor |
|---|---|
| Proyecto | Products & Categories API |
| Versión | 1.0.0 |
| Ambiente | Python 3.x, FastAPI, pytest, TestClient, memoria |
| Versión auditada | Código y pruebas auditadas en bbfed0362c4a9b95a69c841028ae0d1580b6e649; cierre documental posterior en a18881d9214ae24777c6df3bfe4e7caaafadc083; evidencia en `docs/evidencia-pytest.txt` |
| Fecha | Septiembre de 2026 |
| Comando | `pytest -v` |

## 2. Resumen

| Métrica | Resultado |
|---|---:|
| Casos diseñados | 40 automatizados (25 mínimos exigidos) |
| Casos ejecutados | 40 |
| PASSED | 40 |
| FAILED | 0 |
| BLOCKED | 0 |
| NOT EXECUTED | 0 |
| Cobertura de ejecución | 40 / 40 × 100 = 100 % |
| Porcentaje de aprobación | 40 / 40 × 100 = 100 % |
| Defectos críticos abiertos | 0 |

## 3. Retest y regresión

Se registró DEF-001, correspondiente al módulo de Productos inactivo, detectado por inspección del código. Tras la corrección se ejecutó el retest sobre CP-PROD-01, CP-PROD-04, CP-PROD-07, CP-PROD-11, CP-PROD-14, CP-PROD-16, CP-PROD-17 y CP-PROD-18 mediante pytest con selección `-k`: 8 passed. Posteriormente se ejecutó la regresión completa con `pytest -q`: 40 passed, 0 failed. También se añadieron seis pruebas para evitar regresiones en validaciones de payload. DEF-001 quedó en estado Cerrado.

## 4. Criterios de salida

| Criterio | Resultado | Estado |
|---|---|---|
| RF01–RF12 y RN01–RN08 trazados | Matriz completa | Cumplido documentalmente |
| Casos críticos ejecutados | 100 % | Cumplido |
| Al menos 90 % del total ejecutado | 100 % (40/40) | Cumplido |
| Al menos 90 % aprobados | 100 % (40/40) | Cumplido |
| 0 defectos críticos abiertos | 0 confirmados | Cumplido |
| Al menos 15 tests automatizados | 40 tests activos | Cumplido |

## 5. Conclusión técnica

La implementación fue alineada con el contrato evaluable sin eliminar los endpoints existentes de Categorías ni sus filtros, búsqueda y actualización parcial. La suite final produjo 40 PASSED, 0 FAILED, 0 BLOCKED y 0 NOT EXECUTED. La cobertura y aprobación fueron del 100 %, con cero defectos críticos abiertos confirmados; por tanto, los criterios de salida se cumplen para la versión corregida.
