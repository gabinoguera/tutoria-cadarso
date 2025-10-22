# GitHub Copilot Instructions - CADARSO Project

## Project Overview
**Project**: CADARSO - GitHub Copilot Training Repository  
**Purpose**: Educational platform for "Vibecoding" (AI-assisted development) targeting Spanish-speaking IT teams  
**Tech Stack**: Python 3.8+, Jupyter Notebooks, OpenAI API, Pydantic, FastAPI, Pandas, Paramiko (SSH), SAP/ABAP integration  
**Business Context**: Dual business model - luxury hotel + watch retail in Barcelona

## Architecture & Structure

### Content Organization
- `Clase 1/` - Introduction to Vibecoding with SQL examples and tool setup
- `Clase 2/` - Practical use cases (documentation automation, system scripts)  
- `test_apis_marketing.ipynb` - Live demo notebook for multilingual marketing APIs
- `.github/` - Project instructions and templates for standardized development

### Key Learning Patterns
1. **Natural Language → Code**: Transform business requirements into functional scripts
2. **Documentation Generation**: Convert technical code (SAP/ABAP) into user manuals
3. **API Integration**: Build marketing automation with OpenAI APIs
4. **Network Automation**: Create Cisco device management scripts

## Coding Standards

### Style & Formatting
- **Formatter**: Black (Python), Prettier (JavaScript/JSON)
- **Linter**: Flake8 (Python), ESLint (JavaScript)
- **Line length**: 88 characters (Python) / 80 characters (others)
- **Language**: Spanish for comments, docstrings, and variable names in educational context

### Code Quality for Educational Content
- Use type hints in Python for clarity
- Include comprehensive docstrings for all public functions
- Prefer explicit over implicit for learning purposes
- Use meaningful Spanish variable names that relate to business context
- Always include error handling examples
- Add step-by-step logging for educational value

### Example Code Structure
```python
class GestorHotelRelojeria:
    """Gestor principal para automatización de hotel de lujo + relojería."""
    
    def __init__(self, configuracion_cliente: Dict[str, Any]):
        self.logger = self._configurar_logging()
        self.cliente_openai = self._inicializar_openai(configuracion_cliente)
        
    async def proceso_marketing_automatizado(self, tipo_producto: ProductType) -> Dict[str, str]:
        """
        Genera contenido de marketing multiidioma para productos del negocio.
        
        Args:
            tipo_producto: Tipo de producto (hotel_service, luxury_watch, etc.)
            
        Returns:
            Diccionario con contenido en múltiples idiomas
            
        Raises:
            APIError: Error en comunicación con OpenAI
            ValidationError: Error en validación de datos
        """
        self.logger.info(f"Iniciando proceso de marketing para: {tipo_producto.value}")
        # Implementation with error handling and business context
```

## Commit Conventions

**Format**: `<type>(<scope>): <description>`

### Types for Educational Project
- `feat`: Nueva funcionalidad o caso de uso
- `fix`: Corrección de errores en demos o código
- `docs`: Actualización de materiales educativos
- `demo`: Nuevas demos o notebooks interactivos
- `refactor`: Reestructuración de código educativo
- `test`: Añadir/actualizar tests para casos de uso
- `setup`: Configuración de proyecto o herramientas

### Scopes Específicos del Proyecto
- `clase1`: Materiales de introducción al Vibecoding
- `clase2`: Casos de uso prácticos
- `notebook`: Jupyter notebooks y demos interactivas
- `openai`: Integración con APIs de OpenAI
- `cisco`: Scripts de automatización de red
- `sap`: Documentación automática SAP/ABAP
- `hotel`: Casos de uso específicos del hotel
- `relojeria`: Casos de uso específicos de relojería

### Examples
```
feat(notebook): add multilingual marketing API demo
fix(cisco): resolve SSH timeout in device manager script  
docs(clase1): update Vibecoding introduction with new examples
demo(openai): create hotel inventory documentation generator
refactor(utils): extract common validation logic for educational clarity
```

## Development Workflows

### For Educational Content
- Content files use numbered prefixes (`0. guion.md`, `1. herramientas.md`) for workshop flow
- Markdown files contain both Spanish explanations and executable code examples
- Include real business context (hotel inventory, network infrastructure)
- Always provide "Antes/Después" (Before/After) comparisons
- Reference specific line numbers in large files for workshop guidance

### For Demo Code  
- Jupyter notebooks demonstrate live coding sessions
- Use Pydantic models for API data structures (`ProductType`, `ProductSpecs`)
- Include comprehensive error handling patterns
- Add production-ready logging examples
- Show incremental complexity progression

## Project-Specific Conventions

### Language & Audience
- **Primary Language**: Spanish (documentation, comments, variable names)
- **Audience**: Mixed technical levels (IT support teams)
- **Business Context**: Dual business model (luxury hospitality + retail)
- **Teaching Style**: Incremental complexity with practical examples

### Documentation Style
- Use emoji headers for visual learning (`🎯`, `📋`, `🛠️`, `🤖`, `📊`)
- Include both technical specs AND business impact
- Provide detailed code explanations for educational purposes
- Always connect technical concepts to real business scenarios

### Error Handling for Educational Examples
```python
@retry_with_backoff(max_retries=3, base_delay=2)
async def conectar_equipo_cisco(ip_equipo: str, credenciales: Dict[str, str]) -> Dict[str, str]:
    """
    Conecta a equipo Cisco y extrae información del sistema.
    Ejemplo educativo con manejo robusto de errores.
    """
    try:
        ssh_client = paramiko.SSHClient()
        ssh_client.connect(ip_equipo, **credenciales)
        
        # Ejecutar comandos y extraer versión iOS
        stdin, stdout, stderr = ssh_client.exec_command("show version")
        resultado = stdout.read().decode()
        
        return self._extraer_version_ios(resultado)
        
    except paramiko.AuthenticationException:
        self.logger.error(f"Error de autenticación en {ip_equipo}")
        raise AutenticacionError("Credenciales inválidas para equipo Cisco")
        
    except paramiko.SSHException as e:
        self.logger.warning(f"Error SSH en {ip_equipo}: {str(e)}")
        raise ConexionError(f"No se pudo conectar via SSH: {str(e)}")
        
    finally:
        if 'ssh_client' in locals():
            ssh_client.close()
```

## Testing for Educational Content

### Framework & Structure
- **Python**: pytest for all demo code
- **Coverage**: Target >80% for production examples
- **Test Files**: Include test examples for educational value

### Educational Testing Patterns
```python
def test_generador_marketing_hotel_debe_incluir_contexto_lujo():
    """Test educativo: verificar que el marketing incluye elementos de lujo."""
    # Given - Contexto de hotel de lujo
    producto_hotel = ProductSpecs(
        name="Suite Presidencial",
        type=ProductType.HOTEL_SERVICE,
        categoria_lujo="premium"
    )
    
    # When - Generar contenido de marketing
    contenido = generador_marketing.crear_contenido(producto_hotel)
    
    # Then - Verificar elementos de lujo en el contenido
    assert "lujo" in contenido["spanish"].lower()
    assert "luxury" in contenido["english"].lower()
    assert len(contenido["spanish"]) > 100  # Contenido sustancial
```

## Logging & Observability for Educational Examples

### Structured Logging for Learning
```python
import logging
import json
from datetime import datetime

class LoggerEducativo:
    """Logger configurado para ejemplos educativos con contexto de negocio."""
    
    def __init__(self, nombre_componente: str):
        self.logger = logging.getLogger(nombre_componente)
        self._configurar_formato_educativo()
    
    def _configurar_formato_educativo(self):
        """Configura formato JSON estructurado para aprendizaje."""
        formato = logging.Formatter(
            '%(asctime)s - %(name)s - %(levelname)s - %(message)s'
        )
        
        handler = logging.StreamHandler()
        handler.setFormatter(formato)
        self.logger.addHandler(handler)
        self.logger.setLevel(logging.INFO)
    
    def log_proceso_negocio(self, evento: str, contexto: Dict[str, Any]):
        """Log específico para procesos de negocio educativos."""
        mensaje = {
            "evento": evento,
            "contexto_negocio": contexto,
            "timestamp": datetime.now().isoformat(),
            "proposito": "ejemplo_educativo"
        }
        self.logger.info(json.dumps(mensaje, ensure_ascii=False))
```

## Critical Integration Points

### OpenAI API Usage
- All API calls use environment variables for keys (`OPENAI_API_KEY`)
- Implement token usage tracking for cost awareness
- Include bilingual prompt engineering examples (Spanish business context → English API)
- Show error handling for rate limits and API failures
- Educational examples of prompt optimization

### Infrastructure Context
- Network scripts target Cisco devices (SSH connections, IOS commands)
- SAP integration patterns for enterprise data extraction  
- Excel file processing workflows for business data imports
- Real-world authentication and security examples

### Business Context Integration
```python
# Ejemplo de integración de contexto de negocio
class ContextoNegocioHotelRelojeria:
    """Contexto específico para casos de uso educativos."""
    
    TIPOS_PRODUCTOS_HOTEL = [
        "habitaciones_lujo", "servicios_spa", "restaurante_gourmet", 
        "eventos_privados", "concierge_premium"
    ]
    
    TIPOS_PRODUCTOS_RELOJERIA = [
        "relojes_suizos", "joyas_exclusivas", "servicios_personalizacion",
        "reparacion_especializada", "tasacion_profesional"  
    ]
    
    @classmethod
    def obtener_contexto_marketing(cls, tipo_producto: str) -> Dict[str, str]:
        """Proporciona contexto específico para generación de marketing."""
        if tipo_producto in cls.TIPOS_PRODUCTOS_HOTEL:
            return {
                "tono": "elegante_y_acogedor",
                "audiencia": "viajeros_lujo_y_ejecutivos",
                "ubicacion": "Barcelona_centro_historico"
            }
        elif tipo_producto in cls.TIPOS_PRODUCTOS_RELOJERIA:
            return {
                "tono": "exclusivo_y_prestigioso", 
                "audiencia": "coleccionistas_y_conocedores",
                "enfoque": "artesania_y_tradicion_suiza"
            }
```

## Vibecoding Teaching Approach
When generating code for this project:

1. **Show the reasoning process** - explain why each approach works
2. **Include error scenarios** - demonstrate what happens when things go wrong  
3. **Provide incremental complexity** - start simple, build sophistication
4. **Connect to business value** - always explain the practical impact
5. **Use Spanish context** - variable names and comments in Spanish for audience
6. **Include production patterns** - show enterprise-ready code structure
7. **Educational logging** - extensive logging for learning purposes

### Example Prompt Patterns for This Project
```
"Necesito un script que recorra equipos Cisco de un Excel y extraiga versiones de iOS"
→ Generate complete solution with:
  - Excel reading with pandas
  - SSH connection handling with paramiko
  - Error handling and retry logic
  - Structured logging in Spanish
  - Business context (hotel network infrastructure)
  - Educational comments explaining each step

"Crea documentación automática para este código SAP de gestión de inventario"
→ Generate documentation that:
  - Explains technical and business purpose
  - Includes user manual sections
  - Provides troubleshooting guides  
  - Uses Spanish business terminology
  - Shows before/after comparison
```

---

**Last Updated**: October 22, 2025  
**Contact**: Training team for CADARSO project questions  
**Repository**: https://github.com/gabinoguera/tutoria-cadarso